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