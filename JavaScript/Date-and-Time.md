# Javascript

## Syntaxe

```js
new Date()
```

quand l'on ne met pas d'argument, il donne l'heure courante dans le fuseau horaire locale.

Si jamais nous voulons renvoyé une date spécifique nous pouvons faire :

`new Date(année, mois, date, jours, minutes, secondes, ms)`

```js
let May = new Date("2020-04-11");

alert(May)
```

*   Pour l'année, il faut écrire 4 digit (1998) et non (98)
*   Pour le mois, il faut commencer à partir de 0 pour Janvier, 1 pour février etc ...
*   Pour la date, si rien n'est renseigné alors ce sera 1 par défaut
*   Pour les heures, minutes, secondes si rien n'est renseigné alors 00, 00, 00 sera mis par défaut
