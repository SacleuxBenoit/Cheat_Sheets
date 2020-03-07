## Routage

La définition de la route via la doc officiel: 
```
app.METHOD(PATH, HANDLER)
```

*   app c'est l'instance d'express 
```
const express = require('express')
const app = express()
```

*   METHOD peut comprendre : .GET .POST .PUT .DELETE etc, c'est une méthode de [demande http](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)

*   PATH c'est le chemin sur le serveur

*   et HANDLER c'est la fonction éxecutée lorsque la route est mise en correspondance.

## Quelques exemples 

Envoyer Hello World sur la page d'accueil :
```
app.get('/', function(req, send){
    res.send('Hello World');
})
```

Réponse à une demande POST à la racine (/)
```
app.post('/', function (req, res) {
  res.send('Got a POST request');
});
```

Réponse à une demande DELETE sur la route (/user)
```
app.delete('/user', function (req, res) {
  res.send('Got a DELETE request at /user');
});
```