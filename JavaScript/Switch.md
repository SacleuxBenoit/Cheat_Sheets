# JavaScript

## La déclaration de switch

Switch peut remplacer plusieurs `if`, il donne un moyen plus descriptif de comparer une valeur avec plusieurs variantes.

## La syntaxe 

le `switch` a une ou plusieurs `case` et un défaut optionnel.

la syntaxe ressemble à ça :
```
switch(x){
    case 'valeur1': // if (x === 'valeur1')
    ...
    [break]

    case 'valeur2': // if (x === 'valeur2')
    ...
    [break]
    
    defaut:
    ...
    [break]
}
```

* La valeur de `x` est vérifiée avec une égalité strict, pour le 1er case, puis le 2iem etc ...

* Si l'égalité est trouvée, 'switch' commence à exécuter le code commençant par le case correspondant, jusqu'au break le plus proche ou jusqu'à la fin du switch

* si aucun 'case' ne correspond alors le 'defaut' sera exécuté.

