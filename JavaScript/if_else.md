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

L'instruction if peut contenir un bloc `else` il s'éxecute lorsque la condition est incorrecte.

## Plusieurs conditions : "else if" : 

Quand nous voulons tester plusieurs conditions, nous devons utiliser la clause `else if`
il peut y avoir plusieurs else if dans le même block, le dernier else est optionnel.

## Opérateur ternaire "?" :

Parfois nous devons attribuer une variable à une condition

L'opérateur ternaire ou dit "point d'interrogation" nous permet de le faire plus simplement et plus rapidement.

L'opérateur est représenté par un point d'interrogation : `?` il est appellé ternaire parce que l'opérateur a 3 opérandes,

c'est le seul opérateur en JavaScript qui en a autant. 

le syntaxe est : 
```
let resul = condition ? value1 : value2
```

La condition est évaluée, si elle est true, value1 est donc retournée, sinon c'est value2.

par exemple : 
```
let Access = (Age > 18) ? true : false; 
```

nous pouvons omettre les parenthèses autour de `age > 18` l'opérateur point d'interrogation a une faible précédence, il s'éxecute donc après la comparaison >.

mais les parenthèses facilite la lisibilité du code, il est donc conseillé des les utiliser.



