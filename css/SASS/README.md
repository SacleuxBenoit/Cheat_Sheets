# SASS

## c'est quoi SASS 

SASS (qui signifie Syntactically Awesome Style Sheets) est un pré-processeur du langage CSS, il permet de générer du code CSS toute en offrant 
une syntaxe simple et un code réutilisable.

## Comment installer SASS

Pour l'installer avec Linux, il suffit de faire :
```
npm install -g sass
```

et pour l'installer avec Mac : 
```
brew install sass/sass/sass
```

## Comment faire fonctionner le compilateur de SASS 

l'objectif est de créer un fichier SASS et de le compiler, pour ce faire nous allons créer un dossier `Projet`, dedans nous allons
ajouter 2 sous dossiers `SASS` et `CSS`, le dossier SASS va servir à stocker le code SASS et le dossier CSS va être le résultat de 
la compilation.

Ensuite nous allons créer un fichier `style.scss` dans notre dossier `SASS`.

(à noter que les noms des dossiers n'ont pas d'importance, et que l'on peut mettre ce que l'on veut)

### La compilation  

pour compiler le fichier `style.scss` nous allons vérifier le fichier édité avec `watch`, pour cela on va se mettre dans le dossier `Projet`
et écrire `sass --watch scss:css` dans le terminal.

Un fichier `style.css` sera donc créer dans le dossier css, il va être actualisé après chaque sauvegarde du fichier `style.scss`

## Les variables 

avec SASS les variables sont préfixés (comme en php) par un dollar 

Exemple : 

```
$red:#FF0000;
$colorbrick:#B22222;

.cancel{
    border:solid 1px $red;
    background-color: $colorbrick;
}
```
Après la ccompilation ont obtient en css : 
```
.cancel{
    border:solid 1px #FF0000;
    background-color: #B22222
}
```

## Les variables globales 

Pour qu'une variable soit globale il faut la déclarer en dehors d'un bloc de code, car si on déclare la variable dans un bloc de code
elle sera uniquement disponible pour ce bloc en question, SAUF si on fait `!global` après la variable déclaré dans le bloc.
```
$red:#FF0000;
$colorbrick:#B22222;

.cancel{
    $green:#0F0 !global;
    border:solid 1px $red;
    background-color: $colorbrick;
}
.validate{
    border:solid 1px $green;
    background-color: $colorbrick; 
}
```

Apès la compilation on va obtenir : 
```
.cancel{
    border:solid 1px #FF0000;
    background-color: #B22222;
}
.validate{
    border:solid 1px #0F0;
    background-color: #B22222; 
}
```

## Le nesting

Le nesting avec SASS permet d'imbriquer le selecteur d'une manière proche de celui du HTML.

Exemple : 
```
header{ 
    div{   
        p{
            background-color:red;
        }
    }
}
```

Après compilation on va obtenir : 

```
header div p{
    background-color:red;
}
```
il est possible de restructurer les propriétés CSS composées comme (font) :
```
h1{
   font:{ // Ne pas oublier les deux points
      size:15px;
      weight:normal;
      variant:small-caps;
   }
} 
```
ce qui donne après compilation : 

```
h1 {
   font-size: 15px;
   font-weight: normal;
   font-variant: small-caps;
} 
```

## Le mixin 

Le mixin est très utile avec SASS, il s'agit d'un ensemble de style CSS réutilisable.

dans cette exemple nous allons déclarer un mixin du nom de `test` : 
```
@mixin test{
    color :red;
}
```

maintenant que nous avons notre mixin, il suffit de la rapeller la ou on en a besoin :
```
h1{
    @include test;
}
```

après compilation on obtient : 
```
h1{
    color:red;
}
```

ont peut même lui passer des arguments ! :

```
@mixin myTransition($property,$duration,$timing){
   transition-property: $property;
   transition-duration: $duration;
   transition-timing-function: $timing;
}

div{
   &:hover{
      @include myTransition(all, 2s, ease);
   }
} 
```
après la compilation : 
```
div:hover {
   transition-property: all;
   transition-duration: 2s;
   transition-timing-function: ease;
} 
```