## Les bases

## Créer et démarrer une application 

Tout d'abord, il faut créer un dossier, dedans il faut faire un npm init puis installer [Express](installation.md) en tant que dépendance.

une fois fait, nous allons créer un fichier `app.js` et mettre le code ci-dessous dedans : 
```
const express = require('express')
const Router = express()

Router.get('/', function (req, res) {
  res.send('Hello World!')
})

Router.listen(8000, function () {
  console.log('Example app listening on port 8000!')
})
```

Ensuite nous pouvons éxecuter l'application grâce à la commande : `node app.js`, l'application va démarrer un serveur et écouter le port 8000 en affichant `Example app listening on port 8000` dans le terminal, l'application va répondre "Hello World" à la racine (/) et afficher 404 not found pour tous les autres chemins d'accès.