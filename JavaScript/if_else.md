# JavaScript

## Opérateurs Conditionnels : if '?'.

Parfois, nous devons effectuer différentes actions en fonctions d'une condition,
nous devons donc utiiliser l'instruction if et l'opérateur conditionnel '?'

## L'instruction if : 

l'instruction if vérifie une condition entre parenthèses, si le résultat est true il exécute le bloc de code

par exemple : 
```
let year = prompt('In which year was ECMAScript-2015 specification published?', '');
if (year == 2015) alert( 'You are right!' );
```

Dans l'exemple ci-dessus, la condition vérifie une égalité simple (year == 2015)

si il y a + d'exécution à exécuter nous devons alors écrire le code entre des accolades :

```
if (year == 2015) {
  alert( "That's correct!" );
  alert( "You're so smart!" );
}
```

mais il est recommandé de mettre le code entre les accolades même si il n'exécute qu'une seule instruction.

## Conversion Booléenne : 

Un nombre `0` une chaîne de caractères vide `""`, `null`, `undefined` et `NaN` deviennent false 

les autres valeurs deviennent true.

## La clause else : 

L'instruction if peut contenir un bloc `else`il s'éxecue lorsque la condition est incorrecte.