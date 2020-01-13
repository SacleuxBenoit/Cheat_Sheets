# JavaScript

## La déclaration de switch

Switch peut remplacer plusieurs `if`, il donne un moyen plus descriptif de comparer une valeur avec plusieurs variantes.

## La syntaxe 

le `switch` a une ou plusieurs `case` et un défaut optionnel.

la syntaxe ressemble à ça :
```javascript
switch(x){
    case 'valeur1': // if (x === 'valeur1')
    ...
    [break]

    case 'valeur2': // if (x === 'valeur2')
    ...
    [break]
    
    default:
    ...
    [break]
}
```

*   La valeur de `x` est vérifiée avec une égalité strict, pour le 1er case, puis le 2iem etc ...

*   Si l'égalité est trouvée, `switch` commence à exécuter le code commençant par le `case` correspondant, jusqu'au `break` le plus proche ou jusqu'à la fin du `switch`

*   si aucun `case` ne correspond alors le `default` sera exécuté.

## Un exemple 

Un exemple concret de `switch` : 

```javascript
let a = 2 + 2;

switch(a){
    case 3:
      alert('too small');
      break;
    case 4:
      alert('exactly');
    case 5:
      alert('too large');
    default:
    alert('I dont know this values');
}
```