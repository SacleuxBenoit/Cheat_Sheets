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

## setInterval

`setInterval` va nous permettre d'exécuter une fonction / bloc de code en boucle, selon un intervalle défini.

Cette méthode va être utile, lorsque nous voulons réaliser de nombreuses choses, comme une horloge ou encore un timer, qui va se mettre à jours toutes les secondes 

```js
let timer = document.getElementById("timer");
let intervalId;

let jours = 0;
let heures = 0;
let minutes = 0;
let secondes = 0;
let millisecondes = 0;

timer.textContent = jours + ' jours : ' + heures + ' heures : ' + minutes + ' minutes : ' + secondes + ' secondes : ' + millisecondes;

function Timer(){
    intervalId = setInterval(function(){
        timer.textContent = jours + ' jours : ' + heures + ' heures : ' + minutes + ' minutes : ' + secondes + ' secondes : ' + millisecondes;
        millisecondes+=1;
        if(millisecondes >= 10){
            millisecondes = 0;
            secondes += 1;
        }
        if(secondes >= 60){
            secondes = 0;
            minutes += 1;
        }
        if(minutes >= 60){
            minutes = 0;
            heures += 1;
        }
        if(heures >= 24){
            heures = 0;
            jours += 1;
        }
    }, 100)
}
```

## clearInterval 

La méthode `clearInterval` va nous permettre d'arrêter l'exécution en boucle d'une fonction / block de code défini par `setInterval`. 

Si nous voulons stopper le timer de l'exemple pour la partie `setInterval` il suffirait de rajouter :

```js
function PauseTimer(){
    clearInterval(intervalId);
}
```