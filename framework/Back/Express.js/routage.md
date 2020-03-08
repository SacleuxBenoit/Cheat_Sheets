## Routage

La définition de la route via la doc officiel: 
```
app.METHOD(PATH, HANDLER)
```

*   app c'est l'instance d'express 
```js
const express = require('express')
const app = express()
```

*   METHOD peut comprendre : .GET .POST .PUT .DELETE [etc](#etc*), c'est une méthode de [demande http](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)

*   PATH c'est le chemin sur le serveur
*   HANDLER c'est la fonction éxecutée lorsque la route est mise en correspondance.

## Quelques exemples 

Envoyer Hello World sur la page d'accueil :
```js
app.get('/', function(req, send){
    res.send('Hello World');
})
```

Réponse à une demande POST à la racine (/)
```js
app.post('/', function (req, res) {
  res.send('Got a POST request');
});
```

Réponse à une demande DELETE sur la route (/user)
```js
app.delete('/user', function (req, res) {
  res.send('Got a DELETE request at /user');
});
```

## Méthode de routage spéciale

Il existe une méthode de routage spécial qui n'est pas dérivée d'une méthode HTTP : `app.all()`, elle est utilisée pour charger des fonctions middleware à un chemin d'accès pour toutes les méthodes de demande, par exemple :
```js
app.all('/article', function (req, res, next) {
  console.log('Accessing the article section ...');
  next(); // pass control to the next handler
});
```

Alors, pour l'exemple ci-dessus le gestionnaire sera exécuté pour les demandes de /article, que l'on utilise .GET .POST .DELETE etc.

## Notes

<a id="etc*"></a> Voici toutes les méthodes HTTP : : post, get, put, delete, head, options, trace, copy, lock, mkcol, move, purge, propfind, proppatch, unlock, report, mkactivity, checkout, merge, m-search, notify, subscribe, unsubscribe, patch, search, et connect.