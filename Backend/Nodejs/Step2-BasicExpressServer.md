# Step 2 - Basic express server

## Server.js

- import de `express, colors, dotenv`
- Initialisation d'une variable pour le `port`
- Création d'une instance d'express
- faire écouter l'application sur un port spécifique, puis afficher un message dans la console

```js
const express = require("express");
const color = require("colors");
const dotenv = require("dotenv").config();

const port = 2000;

const app = express();

app.listen(port, () => {
  console.log(`Server started on port : ${port}`);
});
```

## Terminal

Création d'un fichier `.env` à la racine du projet

## .env

```.env
NODE_ENV = development
PORT = 2000
```

## server.js

Nous pouvons maintenant changer le `port = 2000` par le port du .env

```js
port = process.env.PORT;
```
