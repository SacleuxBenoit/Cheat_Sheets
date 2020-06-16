# Javascript

## Syntaxe

```js
new Date()
```

quand l'on ne met pas d'argument, il donne l'heure courante dans le fuseau horaire local.

Si jamais nous voulons renvoyer une date spécifique nous pouvons faire :

`new Date(année, mois, date, jours, minutes, secondes, ms)`

```js
let May = new Date("2020-04-11");

alert(May)
```

*   Pour l'année, il faut écrire 4 digits (1998) et non (98)
*   Pour le mois, il faut commencer à partir de 0 pour Janvier, 1 pour février etc ...
*   Pour la date, si rien n'est renseigné alors ce sera 1 par défaut
*   Pour les heures, minutes, secondes si rien n'est renseigné alors 00, 00, 00 sera mis par défaut

Voici un exemple : 

```js
alert(new Date(2020, 0, 1, 0, 0, 0, 0)); // 1 Jan 2020 00:00:00
alert(new Date(2020, 0, 1)); // le même résultat qu'au dessus
```

## Récupérer directement des données grâce à new Date()

Il existe des méthodes pour avoir directement accès à l'année / mois / jour / heures etc : 

Pour les exemples ci-dessous, il va falloir prendre en compte :

```js
let date = new Date()
```

*   Récupérer l'année (avec 4 digits)

```js
date.getFullYear()
```

*   Pour récupérer le mois (de 0 à 11), en partant du principe que janvier = 0

```js
date.getMonth()
```

*   Pour récupérer la date actuelle (entre 1 et 31)

```js
date.getDate()
```

nous pouvons aussi faire la même chose pour les heures, minutes, secondes et millisecondes :

```js
date.getHours()
date.getMinutes()
date.getSecondes()
date.getMillisecondes()
```