# Javascript

## Les types de données  

En Javascript une variable peut contenir n'importe quel type de donnnées, elle peut être à un moment une chaine de caractère, et à un autre moment une valeur numérique.

```javascript
let message = "Hello";
message = 12346;
```

Les langages de programmation qui permettent des choses comme ça sont appelés "typés dynamiquement", ce qui signifie qu'il existe des types de données,
mais que les variables sont liées à aucun d'entre eux.

Il existe 6 types de données `primitives` en Javascript : 

*   [Number](#number)
*   [Boolean](#boolean)
*   [String](#string)
*   [Null](#null)
*   [Undefined](#undefined)
*   [Symbol](#symbol)

## Number <a id="number"></a>

Le type Number sert à la fois pour des nombres entiers comme pour des nombres à virgule.

Il existe de nombreuses opérations pour les nombres comme par exemple : `-` `+` `*` `/` etc.

Il existe aussi des "valeurs numériques spéciales" qui appartiennent également à ce type : `Infinity` `-Infinity` et `NaN`.

`Infinity` représente l'infini en mathématique. C'est une valeur qui est plus grande que n'importe quel nombre.

Nous pouvons l'obtenir à la suite d'une division par zéro, ou encore en le mentionnant directement :
```js
console.log(1 / 0); // Infinity
console.log(Infinity); // Infinity
```

`NaN` représente une erreur de calcul c'est le résultat d'une opération incorrecte ou non définie.

```js
console.log("a string" / 2) // NaN
```

## Boolean <a id="boolean"></a>

Le type `Boolean` à seulement 2 valeurs, `true` et `false`:

*   `true` pour correct
*   `false` pour inccorect

```js
console.log(2 > 4) // False
console.log(2 < 4) // True
```

## String <a id="string"></a>

En Javascript une chaine de caractères doit être entouré par des guillemets, il existe 3 types de guillemet :

*   Les doubles quotes `"Mercure"`
*   Les simples quotes `'Venus'`
*   Les backticks \`Earth\`

Pour Javascript il n'y a pas de réelle différence entre les doubles et les simples quotes. 

Pour les Backticks, ils vont permettre d'insérer des variables et des expressions : 

```js
let planet = "Mars"
console.log(`Tu es sur la planète ${planet}`) // Tu es sur la planète Mars
console.log("Tu es sur la planète ${planet}") // Tu es sur la planète ${planet}
```

Le dernier exemple ci-dessus, ne fonctionne pas car ce ne sont pas des Backticks mais des doubles quotes.

L'expression à l'intérieur de `${}` est évalué, c'est-à-dire que l'on peut mettre à peu près tout ce que l'on veut, ça peut aller d'une variable, à un string ou encore une opération : 

```js
console.log(`il y a ${4 + 4} planètes dans notre système solaire`) // il y a 8 planètes dans notre système solaire 
```

## Null <a id="null"></a>

En javascript, la valeur `Null` représente la "nullité", dans le sens ou aucune valeur n'est présente pour l'objet

## undefined <a id="undefined"></a>

Tout comme `Null` la valeur `undefined` crée son propre type, sa signification est : "aucune valeur n'est affectée"

```js
let pluton;
console.log(pluton) //undefined
```

Techniquement c'est possible d'assigner `undefined` pour une variable en faisant :
```js
let pluton = "planet";
pluton = undefined;
console.log(pluton) // undefined
```

mais cette technique n'est pas recommandée, pour affecter une valeur vide ou inconnue, il est préférable d'utiliser `Null`.
Undefined est plus utilisé pour des vérifications, comme pour voir si une variable a été affectée.

## symbol <a id="symbol"></a>