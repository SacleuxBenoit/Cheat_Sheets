# Javascript

## setTimeout

`setTimeout` va nous servir pour exécuter une fonction / un bloc de code après un temps définit 

cette méthode va demander 2 arguments, la première c'est la fonction à exécuter et la deuxième le temps en millisecondes. c'est ce qui va représenter le délai pour l'exécution de la fonction.

```js
setTimeout(function, milliseconds, param1, param2, ...)
```

## clearTimeout

cette méthode va nous permettre de supprimer ou d'annuler un délai défini avec `setTimeout`

```js
let content; // Création de la variable content

function sayHello(){
    content = setTimeout(function(){alert("Hi")}, 4000); // Ici on dit que la variable content est égal au setTimeout, qui affiche un message au bout de 4 seconde
}

function dontSayHello(){
    clearTimeout(content) // et ici on utilise la méthode clearTimeout pour annuler le délai défini par setTimeout
}
```

avec l'exemple ci-dessus, si l'on crée un bouton `lancer l'alerte` qu'on l'assigne à la fonction `sayHello` et que l'on crée un autre bouton `Stop l'alerte` avec l'assignation de la fonction `dontSayHello`, lorsque nous cliquons sur le bouton `lancer l'alerte` au bout de 4 secondes l'alerte avec le message "Hi" va donc être affiché, par contre si avant les 4 secondes nous cliquons sur le bouton, rien ne sera affiché car `clearTimeout` va annuler le délai définis.