# Nodejs

## Description

### Nodejs c'est quoi ?

Déjà, il faut savoir que Nodejs N'EST PAS un serveur ou un framework, Nodejs c'est une plateforme libre en `Javascript`, c'est un environnement bas niveau qui va permettre l'exécution du javascript côté serveur. Il utilise le moteur Javascript V8 qui est développé par Google (il est open source).

### Créer son serveur HTTP

Contrairement à `PhP`, que l'on associe avec un serveur web HTTP comme `APACHE`, pour Nodejs il va falloir créer sois même le serveur ! 

```js
const http = require('http'); // Le require fait appel à la bibliothèque de Nodejs, ici il fait appel à http

const hostname = '127.0.0.1';  // Ici 127.0.0.1 c'est le localhost
const port = 3000; // configuration du port 

const server = http.createServer((req, res) => {  // Crée un serveur HTTP
  res.statusCode = 200; // Le status code 200 indique la réussite d'une requête
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World'); // Termine le processus et affiche "Hello World"
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

Le code ci-dessus crée un serveur qui renvoie "Hello World" sur le port 3000