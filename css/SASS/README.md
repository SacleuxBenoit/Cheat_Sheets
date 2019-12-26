# SASS

## c'est quoi SASS ?

SASS (qui signifie Syntactically Awesome Style Sheets) est un pré-processeur du langage CSS, il permet de générer du code CSS toute en offrant 
une syntaxe simple et un code réutilisable.

## Comment l'installer ?

Pour l'installer il suffit de faire :
```
npm install -g sass
```

## Comment faire fonctionner le compilateur de SASS ? 

l'objectif est de créer un fichier SASS et de le compiler, pour ce faire nous allons créer un dossier `Projet`, dedans nous allons
ajouter 2 sous dossiers `SASS` et `CSS`, le dossier SASS va servir à stocker le code SASS et le dossier CSS va être le résultat de 
la compilation.

Ensuite nous allons créer un fichier `style.scss` dans notre dossier `SASS`.

(à noter que les noms des dossiers n'ont pas d'importance, et que l'on peut mettre ce que l'on veut)

### La compilation : 

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

