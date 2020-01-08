# JavaScript

## Les types de données  

En JavaScript une variable peut contenir n'importe quelle type de donnnée, elle peut être à un moment une chaine de caractère, et à un autre
moment une valeur numérique.

```javascript
let message = "Hello";
message = 12346;
```

Les langages de programmation qui permettent des choses comme ça sont appelés "typés dynamiquement", ce qui signifie qu'il existe des types de données,
mais que les variables sont liées à aucun d'entre eux.

Il existe 7 types de données de base en JavaScript.

## Number 

Le type Number sert à la fois pour des nombres entiers comme pour des nombres à virgule.

Il existe de nombreuses opérations pour les nombres comme par exemple : `-` `+` `*` `/` etc.

Il existe aussi des "valeurs numérique spéciales" qui appartiennent également à ce type : `Infinity` `-Infinity` et `NaN`.

`Infinity` reprèsente l'infini en mathématique. C'est une valeur qui est plus grande que n'importe quel nombre.

Nous pouvons l'obtenir à la suite d'une division par zéro, ou encore en le mentionnant directement :
```javascript
alert(Infinity);
```

`NaN` représente une erreur de calcul c'est le résultat d'une opération incorrecte ou non définie.

Les valeurs numérique spéciale appartiennent formellement au type "Number" 
