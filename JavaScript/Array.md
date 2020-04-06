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
qu'un tableau commence toujours par l'index 0).

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

## Ajouter un élément au début du tableau

La méthode `unshift` nous permet d'ajouter un ou plusieurs éléments au début du tableau 

```js
const addStart = [2, 923, 2093]
addStart.unshift(300)
console.log(addStart) // Affiche [300, 2, 923, 2093]
```

## Ajouter un élément à la fin du tableau

Pour ajouter un élément à la fin du tableau il faut utiliser la méthode `push`

```js
const addEnd = [2, 923, 2093]
addEnd.push("apple")
console.log(addEnd) // Affiche [2, 923, 2093, "apple"]
```

## Supprimer un élément au début du tableau

Il faut utiliser la méthode `shift` pour supprimer un élément au début du tableau

```js
const deleteStart = ["delete", "not delete"]
deleteStart.shift()
console.log(deleteStart) // Affiche ["not delete"]
```

## Supprimer un élément à la fin du tableau

Pour supprimer un élément à la fin du tableau il faut utiliser la méthode `pop`

```js
const deleteEnd = ["i am still here", "i am delete"]
deleteEnd.pop()
console.log(deleteEnd) // Affiche ["i am still here"]
```

## Trouver l'index d'un élément dans un tableau

Pour trouver l'index d'un élément dans un tableau, il faut utiliser la méthode `indexOf`, il est sensible à la casse il faut donc faire attention de bien mettre la majuscule.

```js
const findIndex = [7687, 0876, 23, 021]
console.log(findIndex.indexOf(23)) // Affiche 2
```

Par contre si l'élément renseigné n'est pas trouvé dans le tableau, `-1` sera affiché

```js
const findIndexFalse = [7687, 0876, 23, 021]
console.log(findIndexFalse.indexOf(25)) // Affiche -1
```

## Trouver l'index du dernier élément que l'on recherche dans le tableau

Par exemple si dans un tableau il y a plusieurs fois la même information mais que nous voulons juste le dernier nous pouvons utiliser `lastIndexOf` pour trouver son index 

```js
const findLastIndex = [1, 2, 12, 192, 11,234, 901, 11]
console.log(findLastIndex.lastIndexOf(11)) // Affiche 7
```

tout comme `indexOf`, si l'élément renseigné n'est pas trouvé dans le tableau, `-1` sera affiché

## Supprimer un ou plusieurs élément grâce à leurs index

Pour supprimer un ou plusieurs élément dans un tableau, il faut utiliser la méthide `splice`

```js
const deleteElem = ["Apple", "Orange", "Bananas", 123]
deleteElem.splice(2,2)
console.log(deleteElem) // Affiche ["Apple", "Orange"]
```

Comme nous pouvons le voir dans l'exemple au-dessus, la méthode `splice` prend 2 paramètres le 1er c'est l'index et le deuxième c'est le nombre d'éléments à supprimer