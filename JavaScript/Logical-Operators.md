# Javasript

## Opérateur logique

En javascript il existe 3 types d'opérateur logique : OR `||`, AND `&&`, NOT `!`, ils peuvent être appliqués à tous types de valeurs.

### L'opérateur OR ||

Voici la syntaxe : 

```js
result = true || false
```

Il faut savoir que :

*   l'opérateur `OR` évalue l'opérande de la gauche vers la droite
*   il converti chaque opérande en booléen
*   si le résultat est `true ` alors il s'arrête et retourne la valeur
*   si tous les opérandes sont `false` alors il retourne le dernier opérande

il y a 4 combinaisons possibles : 

```js
alert( true || true );   // true
alert( true || false );  // true
alert( false || true );  // true
alert( false || false ); // false
```

comme nous pouvons le voir le résultat est toujours `true` sauf quand tous les opérandes sont `false`.

La plupart du temps `||` s'utilise avec un `if`

```js
let heure = 19;

if (heure < 8 || heure > 18) {
  alert( 'Le bureau est fermé' );
}
```

### L'opérateur AND &&

Voici la syntaxe : 

```js
result = a && b
```

contrairement à `||`, `&&` retourne `true` uniquement si les 2 opérandes sont `true` :

```js
alert( true && true );   // true
alert( true && false );  // false
alert( false && true  );  // false
alert( false && false ); // false
```

tout comme `||`, `&&` s'utilise souvent avec `if`

```js
let Heure = 00;
let Minute = 00;
let Seconde = 00;

if(Heure == 00 && Minute == 00 && Seconde == 00){
    alert("We have a Lift-off !")
}
```

il faut savoir que `&&` ne recherche pas les valeurs `true` mais il recherche la première valeur `false` ! si une valeur `false` est trouvée alors l'opérande sera automatiquement `false`

Pour ce qui est de la précédence, `AND` est plus grand que `OR` donc pour `1 && 2 || 3 && 4` c'est comme ci c'était `(1 && 2) || (3 && 4)`

### L'opérateur NOT !

Voici la syntaxe :

```js
result = !x
```

L'opérateur accepte un seul argument et le transforme en `true` ou `false` et retourne l'inverse de la valeur.

Nous pouvons traduire `!` par `est différent de`

Par exemple 

```js
let a = 2

if(a != 2){
    console.log("La valeur est différent de 2")
} else{
    console.log("La valeur est égale à 2")
}
```

Le double `!!` permet de convertir la valeur en `BOOLEAN`

```js
alert(!!"un string non vide") // true
alert(!!"") // false
```

En résumé pour `!!` le 1er point d'exclamation convertie la valeur en booléen, et le deuxième point d'exclamation change une fois de plus la valeur en Booléen et la retourne.