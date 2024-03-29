# SASS

## c'est quoi SASS 

SASS (qui signifie Syntactically Awesome Style Sheets) est un préprocesseur du langage CSS, il permet de générer du code CSS toute en offrant 
une syntaxe simple et un code réutilisable.

## Comment installer SASS

Pour l'installer avec Linux, il suffit de faire :
```bash
npm install -g sass
```

et pour l'installer avec Mac : 
```bash
brew install sass/sass/sass
```

## Comment faire fonctionner le compilateur de SASS 

l'objectif est de créer un fichier SASS et de le compiler, pour ce faire nous allons créer un dossier `Projet`, dedans nous allons
ajouter 2 sous-dossiers `SASS` et `CSS`, le dossier SASS va servir à stocker le code SASS et le dossier CSS va être le résultat de la compilation.

Ensuite nous allons créer un fichier `style.scss` dans notre dossier `sass`.

(à noter que les noms des dossiers n'ont pas d'importance, et que l'on peut mettre ce que l'on veut)

### La compilation  

pour compiler le fichier `style.scss` nous allons vérifier le fichier édité avec `watch`, pour cela on va se mettre dans le dossier `Projet`
et écrire `sass --watch sass:css` dans le terminal.

Un fichier `style.css` sera donc créé dans le dossier `CSS`, il va être actualisé après chaque sauvegarde du fichier `style.scss`

## Les variables 

avec SASS les variables sont préfixées (comme en Php) par un dollar 

Exemple : 

```scss
$red:#FF0000;
$colorbrick:#B22222;

.cancel{
    border:solid 1px $red;
    background-color: $colorbrick;
}
```
Après la compilation on obtient en Css : 
```css
.cancel{
    border:solid 1px #FF0000;
    background-color: #B22222
}
```

## Les variables globales 

Pour qu'une variable soit globale il faut la déclarer en dehors d'un bloc de code, car si on déclare la variable dans un bloc de code
elle sera uniquement disponible pour ce bloc en question, SAUF si on fait `!global` après la variable déclarée dans le bloc.
```scss
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

Après la compilation on va obtenir : 
```css
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

Le nesting avec SASS permet d'imbriquer le sélecteur d'une manière proche de celui du HTML.

Exemple : 
```scss
header{ 
    div{   
        p{
            background-color:red;
        }
    }
}
```

Après compilation on va obtenir : 

```css
header div p{
    background-color:red;
}
```
il est possible de restructurer les propriétés CSS composées comme (font) :
```scss
h1{
   font:{ // Ne pas oublier les deux points
      size:15px;
      weight:normal;
      variant:small-caps;
   }
} 
```
ce qui donne après compilation : 

```css
h1 {
   font-size: 15px;
   font-weight: normal;
   font-variant: small-caps;
} 
```

## Le mixin 

Le mixin est très utile avec SASS, il s'agit d'un ensemble de style CSS réutilisable.

dans cette exemple nous allons déclarer un mixin du nom de `test` : 
```scss
@mixin test{
    color :red;
}
```

maintenant que nous avons notre mixin, il suffit de la rappler là où on en a besoin :
```scss
h1{
    @include test;
}
```

après compilation on obtient : 
```css
h1{
    color:red;
}
```

on peut même lui passer des arguments ! :

```scss
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
```css
div:hover {
   transition-property: all;
   transition-duration: 2s;
   transition-timing-function: ease;
} 
```

## Les partials

Nous pouvons créer un fichier partial qui va contenir un petit bout de code, ce bout de code va pouvoir être importé dans nos autres fichiers. 

Par exemple si nous avons besoin d'utiliser la même palette de couleurs pour plusieurs fichiers, nous allons créer `_colors.scss`
(l'underscore spécifie à SASS que c'est un fichier partial et ne va pas générer de fichier css)
et l'importer dans nos fichiers avec `@import "colors"` il n'y a pas besoin d'utiliser l'underscore pour l'import

ça va donner quelque chose comme : 
```scss
/* Partial _color.scss */
$colorBackground:#141414;
$colorContainer:#1f1f1f;
$colorBorder:#3b3a3a;
```

```scss
/* commentSection.scss */
.containerCommentSection{
    @import "colors";

    background-color: $colorContainer; /* $colorContainer = #1f1f1f */
    border: 1px solid $colorBorder; /* $colorBorder = #3b3a3a */
    margin-top: .5rem;
}
```