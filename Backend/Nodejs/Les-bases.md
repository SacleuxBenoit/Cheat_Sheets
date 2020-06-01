# Nodejs

## Description

### Nodejs c'est quoi ?

Déjà, il faut savoir que Nodejs N'EST PAS un serveur ou un framework, Nodejs c'est une plateforme libre en `Javascript`, c'est un environnement bas niveau qui va permettre l'exécution du javascript côté serveur. Il utilise le moteur Javascript V8 qui est développé par Google (il est open source).

### Créer son serveur HTTP

Contrairement à `PhP`, que l'on associe avec un serveur web HTTP comme `APACHE`, pour Nodejs il va falloir créer sois même le serveur ! 

```js
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

