# Javascript 

## Description

Les tableaux sont des objets qui possèdent des méthodes incorporées, ni la taille du tableau ni les éléments n'est fixe, puisque nous pouvons ajouter ou enlever des éléments dedans.
Voici la syntaxe :

```js
const arr = ["Elem1", "Elem2", "Elem3"]
```

Il faut savoir que le premier élément d'un tableau est TOUJOURS l'index 0 ! 

## connaître le nombre d'éléments dans un tableau

Pour connaître le nombre d'éléments dans un tableau c'est assez facile il suffit d'utiliser `.length` 

Exemple :

```js
const Myarr = ["apple", "bananas", "orange", "lemon"]
console.log(Myarr.length)
```

On peut donc voir dans la console : `4`, c'est le nombre d'éléments dans le tableau.


## Trouver un élément dans un tableau grâce à son index

Pour trouver un élément d'un tableau en connaissant son index il va falloir faire comme ci-dessous (il ne faut pas oublier
qu'un tableau commence toujours pas l'index 0).

```js
const findElem = ["index0", "index1", "index2","index3"]
console.log(findElem[1])
```

dans la console `index1` va donc être affiché.

## Trouver le dernier élément dans un tableau

La propriété `length-1` va nous donner le dernier élément d'un tableau, pourquoi mettre `-1`? car un tableau commence toujours par l'index 0.

```js
const last = [3, 8, 238, 278]
console.log(last[last.length-1]) // Affiche 278
```