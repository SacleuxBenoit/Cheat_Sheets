# Javascript

## Les fonctions 

### Description

Une fonction c'est un ensemble d'instructions pouvant effectuer une tâche, les fonctions font parties des briques fondamentales de Javascript, il existe des fonctions intégrées comme [Alert Prompt et Confirm](AlertPromptConfirm.md), mais nous pouvons aussi créer les nôtres.

### Pourquoi utiliser une fonction

Par exemple : nous avons 2 boutons : `Joueur 1` et `Joueur 2`, lorsque l'on clique sur le bouton `Joueur 1` son score augmente de 1, pareil pour le `joueur 2`. Au lieu d'écrire 2 fois le même code pour chaque bouton, nous pouvons mettre le code dans une fonction et appeler la fonction pour le bouton `Joueur 1` et `Joueur 2`, cela nous évite donc de réécrire (ou de copier collé :) ) le même code plusieurs fois.

### Créer une fonction

Pour créer une fonction (on dit qu'on la déclare) il suffit de mettre le mot `function`, suivi du nom de la fonction et de parenthèses, dans les parenthèses on va mettre nos arguments.

```js
function NameFunction(arg1, arg2){
    // Instructions
}
```

lorsque nous déclarons une fonction, celle-ci n'est pas exécuté, mais elle est gardé en mémoire pour être exécutée quand on va l'appeler.

### Appeler une fonction

Pour appeler une fonction il suffit de mettre le nom de la fonction suivie de parenthèses. Une fois ceci fait la fonction sera exécuté.

```js
function conversion(){
    let message= prompt("Entrez la valeur en miles"); // Demande d'entrer une valeur en miles
    let resultat = message * 1.60934; // Fait la conversion en Km
    alert(message + " miles est égal à " + resultat + " Km") // Affiche un message avec "Alert"
}

conversion() // Appel de la fonction
```

La fonction ci-dessus va afficher un prompt et demander une valeur en miles, une fois que l'utilisateur auras entré sa valeur, 
la fonction va faire la conversion des miles en km, puis affiché un message donnant le résultat.

### Créer une fonction avec un argument

Rappel : pour mettre un argument dans une fonction il suffit de l'écrire dans les parenthèses après le nom de la fonction : 

```js
function convertisseur(change){
    let miles = prompt("Entrez votre valeur en miles");
    let result = miles * change;
    alert(miles + " miles est égal à " + result + " Km")
}

convertisseur(1.60934)
```

Il est tout à fait possible de mettre un deuxième argument, il faut juste mettre une virgule après le 1er. Ensuite quand nous allons appeler notre fonction, il suffira de donner les paramètres dans le même ordre.

## Les fonctions expressions

Précédemment nous avons vu comment créer une fonction, il faut savoir qu'il existe d'autres sortes de fonction, nous allons maintenant voir les `Function expression` 

```js
let Hello = function(){
    alert("Hello")
};
```

La fonction est assignée à une variable, peu importe ce qu'il y a dans la fonction, elle va être stockée dans la variable `Hello` (il ne faut pas oublier de mettre le point-virgule à la fin, car c'est une variable).

La différence entre une fonction classique et celle-là, c'est que dans la fonction classique toute la fonction est chargée dans la mémoire du navigateur, même si elle n'est pas utilisée immédiatement, à la différence des `function expression` qui sont appelées quand l'interpréteur atteint leur ligne de code. 

Nous pouvons copier une fonction dans une autre variable : 

```js
let Hello = function(){ // création de la fonction 
    alert("Hello")
};

let Hi = Hello // copie de la fonction dans la variable Hi

Hello() // Hello
Hi() // Hello
```

## les fonctions fléchées

Il y a une autre syntaxe pour les fonctions : les `Arrow functions`

```js
let Goodbye = (arg1, arg2) => Expression ;
```

on crée une fonction `Goodbye` qui prend `arg1` et `arg2` en argument et qui évalue `Expression`

c'est beaucoup plus court que ceci : 

```js
let Goodbye = function(arg1, arg2){
    return expression
};
```

Si nous n'avons qu'un seul argument, les parenthèses ne sont pas obligatoires par exemple :

```js
let Km = miles => miles * 1,60934;
```

ce qui donnerait avec une function expression

```js
let Km = function(miles){
    return miles * 1,60934
}
```

par contre s'il n'y a pas d'argument les parenthèses sont obligatoire

```js
let Mage = () => alert("I'm a Mage")
```

Maintenant, si nous avons besoin d'écrire une `Arrow function` sur plusieurs lignes il va falloir utiliser les accolades :

```js
let Division = (a,b) => {
    let result = a / b;
    return result
}
```