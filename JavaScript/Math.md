# Javascript

## Description

`Math` c'est un objet natif dont les méthodes et propriétés permettent l'utilisation de fonctions et constantes mathématiques.

## Les propriétés

`Math` est disponible avec 8 propriétés : 

*   `Math.E` C'est une constante mathématique, le nombre d'Euler vaut environ 2,71828

```js
console.log(Math.E) // Affiche 2.718281828459045
```
*   `Math.LN2` ça représente la valeur du logarithme naturel de 2, c'est environ 0,693

```js
console.log(Math.LN2); // Affiche 0.6931471805599453

```
*   `Math.LN10` représente la valeur du logarithme naturel de 10, c'est environ 2,302

```js
console.log(Math.LN10); // Affiche 2.302585092994046
```

*   `Math.log2(x)` représente la valeur du logarithme en base 2, environ 1,442 

```js
console.log(Math.log2(3)) // Affiche 1.584962500721156
console.log(Math.log2(0)) // Affiche -infinity
console.log(Math.log2(-3)) // Affiche NaN
```

*   `Math.log10(x)` représente la valeur du logarithme en base 10, environ 0,434 :

```js
console.log(Math.log10(3)) // Affiche 0.47712125471966244
console.log(Math.log10(0)) // Affiche -infinity
console.log(Math.log10(-3)) // Affiche NaN
```

*   `Math.PI`  c’est le rapport constant de la circonférence d’un cercle à son diamètre dans un plan euclidien, environ 3.141592

```js
console.log(Math.PI) // Affiche 3.141592653589793

// Cette fonction utilise Math.PI pour calculer la circonférence d'un cercle avec un rayon donné
function circonference(radius){
return  Math.PI * (radius + radius);
}
console.log(circonference(2)); // Affiche 12.566370614359172
```

*   `Math.SQRT1_2` c'est la racine carrée de 1/2, environ 0,707

```js
console.log(Math.SQRT1_2) // Affiche 0.7071067811865476

```
*   `Math.SQRT2` c'est la racine carrée de 2, environ 1.414

```js
console.log(Math.SQRT2) // Affiche 1.4142135623730951
```

## Méthodes

Les méthodes sont : 

*   `Math.abs(x)` Retourne la valeur [absolue](https://fr.wikipedia.org/wiki/Valeur_absolue) d'un nombre

```js
console.log(Math.abs(11)) // Affiche 11
console.log(Math.abs(-11)) // Affiche 11
```
*   `Math.sqrt(x)` Retourne la racine carré d'un nombre 

```js
console.log(Math.sqrt(6)) // Affiche 2.449489742783178
console.log(Math.sqrt(-0))
console.log(Math.sqrt(-6)) // Affiche NaN
```
*   `Math.sin(x)` Retourne le sinus d'un nombre

```js
console.log(Math.sin(8)) // Affiche 0.9893582466233818
console.log(Math.sin(-8)) // Affiche -0.9893582466233818
console.log(Math.sin(0)) // Affiche 0
```
*   `Match.sinh(x)` Retourne le sinus hyperbolique d'un nombre

```js
console.log(Math.sinh(8)) // Affiche 1490.4788257895502
console.log(Math.sinh(-8)) // Affiche -1490.4788257895502
console.log(Math.sinh(0)) // Affiche 0
```
*   `Math.cos(x)` Retourne le cosinus d'un nombre

```js
console.log(Math.cos(4)) // Affiche -0.6536436208636119
console.log(Math.cos(-4)) // Affiche -0.6536436208636119
console.log(Math.cos(0)) // Affiche 1
```
*   `Match.cosh(x)` Retourne le cosinus hyperbolique d'un nombre

```js
console.log(Math.cosh(4)) // Affiche 27.308232836016487
console.log(Math.cosh(-4)) // Affiche 27.308232836016487
console.log(Math.cosh(0)) // Affiche 1
```
*   `Math.acos(x)` Retourne l'arc cosinus d'un nombre

```js
console.log(Math.acos(1)) // Affiche 0
console.log(Math.acos(-1)) // Affiche 3.141592653589793
console.log(Math.acos(0)) // Affiche 1.5707963267948966
console.log(Math.acos(-2)) // Affiche NaN
```
*   `Math.acosh(x)` Retourne l'arc cosinus hyperbolique d'un nombre, retourne NaN si le nombre est plus petit que 1

```js
console.log(Math.acosh(6)) // Affiche 2.477888730288475
console.log(Math.acosh(0)) // Affiche NaN
```
*   `Math.asin(x)` Retourne l'arc sinus d'un nombre

```js
console.log(Math.asin(1)) // Affiche 1.5707963267948966
console.log(Math.asin(-1)) // Affiche -1.5707963267948966
console.log(Math.asin(0)) // Affiche 0
```
*   `Math.asinh(x)` Retourne l'arc sinus hyperbolique d'un nombre

```js
console.log(Math.asinh(1)) // Affiche 0.881373587019543
console.log(Math.asinh(-1)) // Affiche -0.881373587019543
console.log(Math.asinh(0)) // Affiche 0
```
*   `Math.tan(x)` Retourne la tangente d'un nombre
la fonction ci-dessous calcul la tangente après avoir converti l'argument en radians

```js
function getTanDeg(deg) {
  const rad = deg * Math.PI/180;
  return Math.tan(rad);
}
console.log(getTanDeg(45)) // Affiche 0.9999999999999999
```
*   `Math.tanh(x)` Retourne la tangente hyperbolique d'un nombre

```js
console.log(Math.tanh(0)) // Affiche 0
console.log(Math.tanh(1)) // Affiche 0.7615941559557649
console.log(Math.tanh(Infinity)) // Affiche 1 
```
*   `Math.atan(x)` Retourne l'arc tangente d'un nombre

```js
console.log(Math.atan(2)) // Affiche 1.1071487177940906
console.log(Math.atan(-2)) // Affiche -1.1071487177940906
console.log(Math.atan(Infinity)) // Affiche 1.5707963267948966
console.log(Math.atan(-Infinity)) // Affiche -1.5707963267948966
```
*   `Math.atanh(x)` Retourne l'arc tangente hyperbolique d'un nombre
Pour les valeurs strictement inférieures à -1 ou strictement supérieures à 1, NaN sera renvoyé

```js
console.log(Math.atanh(0)) // Affiche 0
console.log(Math.atanh(1)) // Affiche Infinity
console.log(Math.atanh(2)) // Affiche NaN
console.log(Math.atanh(-2)) // Affiche NaN
```
*   `Math.cbrt(x)` Retourne la racine cubique d'un nombre

```js
console.log(Math.cbrt(1)) // Affiche 1
console.log(Math.cbrt(-1)) // Affiche -1
console.log(Math.cbrt(Infinity)) // Affiche Infinity
console.log(Math.cbrt(null)) // Affiche 0
console.log(Math.cbrt(2)) // Affiche 1.2599210498948732
```
*   `Math.clz32(x)` Retourne le nombre de 0 qui préfixent un entier sur 32 bits
clz32 est un raccourcis pour CountLeadingZeroes32
```js
console.log(Math.clz32(1)) // Affiche 31
console.log(Math.clz32(100)) // Affiche 25
console.log(Math.clz32(false)) // Affiche 32
```
*   `Math.exp(x)` Retourne l'exponentielle d'un nombre (E'nombre), E = la constante d'Euler

```js
console.log(Math.exp(2)) // Affiche 7.38905609893065
console.log(Math.exp(-2)) // Affiche 0.1353352832366127
console.log(Math.exp(Infinity)) // Affiche Infinity
```
*   `Math.ceil(x)` Retourne le plus petit entier supérieur ou égal à la valeur passé en paramètre

```js
console.log(Math.ceil(7.015)) // Affiche 8 dans la console
```
*   `Math.floor(x)` Retourne le plus grand entier inférieur ou égal à la valeur passé en paramètre

```js
console.log(Math.floor(7.915)) // Affiche 7 dans la console
```
*   `Math.fround(x)` Retourne le nombre flottant exprimé sur 32 bits le plus proche de l'argument

```js
console.log(Math.fround(2)) // Affiche 2
console.log(Math.fround(-2)) // Affiche -2
console.log(Math.fround(2,788)) // Affiche 2
console.log(Math.fround(false)) // Affiche 0
```
*   `Math.hypot([x[,y[,...]]])` Retourne la racine carré de la somme des carrés des arguments

```js
console.log(Math.hypot()) // Affiche 0
console.log(Math.hypot(5, 7)) // Affiche 8.602325267042627
console.log(Math.hypot(5, 7, "test")) // Affiche "NaN"
console.log(Math.hypot(-4)) // Affiche 4
```
*   `Math.imul(x,y)` Retourne le résultat de la multiplication d'entiers sur 32 bits

```js
console.log(Math.imul(5, 7)) // Affiche 35
console.log(Math.imul(-5, 7)) // Affiche -35
console.log(Math.imul(0, 7)) // Affiche 0
```
*   `Math.log(x)` Retourne le logarithme naturel (log'e') d'un nombre

```js
console.log(Math.log(-2)) // Affiche NaN
console.log(Math.log(2)) // Affiche 0.6931471805599453
console.log(Math.log(0)) // Affiche -Infinity
console.log(Math.log(5)) // Affiche 1.6094379124341003
```
*   `Math.log1p(x)` Retourne le logarithme naturel de 1+ d'un nombre
*   `Math.log10(x)` Retourne le logarithme naturel en base 10 d'un nombre
*   `Math.log2(x)` Retourne le logarithme naturel en base 2 d'un nombre
*   `Math.max([x[,y[...]]])` Retourne la plus grande valeur d'une liste de nombre

```js
const arr = [-4, 5, -3, 15]
console.log(Math.max(...arr)); // Affiche 15 dans la console
```

*   `Math.min([x[,y[...]]])` Retourne la plus petite valeur d'une liste de nombre

```js
const array = [-4, 5, -3, 15]
console.log(Math.min(...array)); // Affiche -4 dans la console 
```

*   `Math.pow(x,y)` Retourne le calcul de x à la puissnace y (x = la base et y = l'exposant)

```js
console.log(Math.pow(4, 4)) // Affiche 256 = 4*4*4*4
console.log(Math.pow(4, 6/3)) // Affiche 16
```
*   `Math.random()` Retourne un nombre aléatoire compris entre 0 et 1, 0 étant inclus et 1 exclu
 
```js
function entierAleatoire(min,max){
    return Math.floor(Math.random() * (max - min + 1) + min);
}
const entier = entierAleatoire(1,10);
console.log(entier) // Affiche un nombre aléatoire compris entre 1 et 10

```

*   `Math.round(x)` Retourne l'arrondi d'un nombre 

```js
console.log(Math.round(3.33)) // Affiche 3
console.log(Math.round(3.5)) // Affiche 4
console.log(Math.round(3.85)) // Affiche 4
console.log(Math.round(3.85*100)/100) // Affiche 3.85
```

*   `Math.sign(x)` Retourne le signe d'un nombre, c'est-à-dire s'il est positif négatif ou égal à zéro

`Math.sign()` peut renvoyer 5 valeurs : `1, -1, 0, -0, NaN`, qui indique respectivement que x est un nombre positif,négatif, zéro, la limite négative du zéro et Not a Number

```js
console.log(Math.sign(2)) // Affiche 1
console.log(Math.sign(-2)) // Affiche -1
console.log(Math.sign(0)) // Affiche 0
console.log(Math.sign(-0))  // Affiche -0
console.log(Math.sign("test")) // Affiche NaN
```
*   `Math.toSource()` Retourne la chaine de caractères "Math"
*   `Math.trunc(x)` Retourne la partie entière d'un nombre (la partie décimale est retirée)