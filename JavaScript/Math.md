# Javascript

## Description

`Math` c'est un objet natif dont les méthodes et propriétés permettent l'utilisation de fonctions et constantes mathématiques.

## Les propriétés

`Math` est disponible avec 8 propriétés : 

*   `Math.E` C'est une constante mathématique, le nombre dEuler vaut environ 2,71828
*   `Math.LN2` ça représente la valeur du logarithme naturel de 2, c'est environ 0,693
*   `Math.LN10` représente la valeur du logarithme naturel de 10, c'est environ 2,302
*   `Math.LOG2E` représente la valeur du logarithme en base 2 de e, environ 1,442 
*   `Math.LOG10E` représente la valeur du logarithme en base 2 de e, environ 0,434 :
*   `Math.PI`  c’est le rapport constant de la circonférence d’un cercle à son diamètre dans un plan euclidien, environ 3.141592
*   `Math.SQRT1_2` c'est la racine carrée de 1/2, environ 0,707
*   `Math.SQRT2` c'est la racine carrée de 2, environ 1.414

## Méthodes

Les méthodes sont : 

*   `Math.abs(x)` Retourne la valeur [absolue](https://fr.wikipedia.org/wiki/Valeur_absolue) d'un nombre
*   `Math.sqrt(x)` Retourne la racine carré d'un nombre 
*   `Math.sin(x)` Retourne le sinus d'un nombre
*   `Match.sinh(x)` Retourne le sinus hyperbolique d'un nombre
*   `Math.cos(x)` Retourne le cosinus d'un nombre
*   `Match.cosh(x)` Retourne le cosinus hyperbolique d'un nombre
*   `Math.acos(x)` Retourne l'arc cosinus d'un nombre
*   `Math.acosh(x)` Retourne l'arc cosinus hyperbolique d'un nombre
*   `Math.asin(x)` Retourne l'arc sinus d'un nombre
*   `Math.asinh(x)` Retourne l'arc sinus hyperbolique d'un nombre
*   `Math.tan(x)` Retourne la tangente d'un nombre
*   `Math.tah(x)` Retourne la tangente hyperbolique d'un nombre
*   `Math.atan(x)` Retourne l'arc tangente d'un nombre
*   `Math.atanh(x)` Retourne l'arc tangente hyperbolique d'un nombre
*   `Math.atan2(y,x)` Retourne l'arc tangente du quotient de ses arguments
*   `Math.cbrt(x)` Retourne la racine cubique d'un nombre
*   `Math.ceil(x)` Retourne le plus petit entier supérieur ou égal à la valeur passé en paramètre
*   `Math.clz32(x)` Retourne le nombre de 0 qui préfixent un entier sur 32 bits
*   `Math.exp(x)` Retourne l'exponentielle d'un nombre (E'nomre), E = la constante d'Euler
*   `Math.expml(x)` Retourne le résultat de 1- l'exponentielle d'un nombre
*   `Math.floor(x)` Retourne le plus grand entier inférieur ou égal à la valeur passé en paramètre
*   `Math.fround(x)` Retourne le nombre flottant exprimé sur 32 bits le plus proche de l'argument
*   `Math.hypot([x[,y[,...]]])` Retourne la racine carré de la somme des carrés des arguments
*   `Math.imul(x,y)` Retourne le résultat de la multiplication d'entiers sur 32 bits
*   `Math.log(x)` Retourne le logarithme naturel (log'e') d'un nombre
*   `Math.log1p(x)` Retourne le logarithme naturel de 1+ d'un nombre
*   `Math.log10(x)` Retourne le logarithme naturel en base 10 d'un nombre
*   `Math.log2(x)` Retourne le logarithme naturel en base 2 d'un nombre
*   `Math.max([x[,y[...]]])` Retourne la plus grande valeur d'une liste de nombre

Exemple : 
```js
const arr = [-4, 5, -3, 15]
console.log(Math.max(...arr)); // Affiche 15 dans la console
```
*   `Math.min([x[,y[...]]])` Retourne la plus petite valeur d'une liste de nombre

Exemple : 
```js
const array = [-4, 5, -3, 15]
console.log(Math.min(...array)); // Affiche -4 dans la console 
```

*   `Math.pow(x,y)` Retourne le calcul de x à la puissnace y (x = la base et y = l'exposant)
*   `Math.random()` Retourne un nombre aléatoire compris entre 0 et 1, 0 étant inclus et 1 exclu

Exemple : 
```js
function entierAleatoire(min,max){
    return Math.floor(Math.random() * (max - min + 1) + min);
}
const entier = entierAleatoire(1,10);
console.log(entier) // Affiche un nombre aléatoire compris entre 1 et 10

```
*   `Math.round(x)` Retourne l'arrondi d'un nombre 
*   `Math.sign(x)` Retourne le signe d'un nombre, c'est-à-dire s'il est positif négatif ou égal à zéro
*   `Math.toSource()` Retourne la chaine de caractères "Math"
*   `Math.trunc(x)` Retourne la partie entière d'un nombre (la partie décimale est retirée)