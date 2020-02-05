# Javascript

## Les types de données  

En Javascript une variable peut contenir n'importe quel type de donnnées, elle peut être à un moment une chaine de caractère, et à un autre
moment une valeur numérique.

```javascript
let message = "Hello";
message = 12346;
```

Les langages de programmation qui permettent des choses comme ça sont appelés "typés dynamiquement", ce qui signifie qu'il existe des types de données,
mais que les variables sont liées à aucun d'entre eux.

Il existe 7 types de données de base en Javascript.

## Number 

Le type Number sert à la fois pour des nombres entiers comme pour des nombres à virgule.

Il existe de nombreuses opérations pour les nombres comme par exemple : `-` `+` `*` `/` etc.

Il existe aussi des "valeurs numériques spéciales" qui appartiennent également à ce type : `Infinity` `-Infinity` et `NaN`.

`Infinity` représente l'infini en mathématique. C'est une valeur qui est plus grande que n'importe quel nombre.

Nous pouvons l'obtenir à la suite d'une division par zéro, ou encore en le mentionnant directement :
```javascript
alert(Infinity);
```

`NaN` représente une erreur de calcul c'est le résultat d'une opération incorrecte ou non définie.

Les valeurs numériques spéciales appartiennent formellement au type "Number" 
