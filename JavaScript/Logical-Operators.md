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

comme nous pouvons le voir le résultat est toujours `true`sauf quand tous les opérandes sont `false`.

La plupart du temps `||` s'utilise avec un `if`

```js
let heure = 19;

if (heure < 8 || heure > 18) {
  alert( 'Le bureau est fermé' );
}
```