# Step 1 - init project

## Initialisation des dossiers

- Création du fichier .gitignore
- Ajout de node_modules et de .env dans le .gitignore

- Création du dossier backend, puis server.js dans ce même-dossier
  - server.js : `console.log("Hello World)`

## Racine du projet

- npm init > changer l'entry point en server.js
- npm i express dotenv(1) mongoose(2) colors
- npm i -D nodemon(3)

## Package.json

```json
"scripts":{
    "start": "node backend/server.js",
    "dev": "nodemon backend/server.js"
}
```

Il suffit maintenant de faire un npm run dev dans le terminal pour faire apparaître le `Hello World`

# Notes

Le module dotenv est utile pour gérer les variables d'environnement, il permet de stocker des configurations sensible, telles que des clés d'API, des identifiants de base de données, des token d'authentication etc

Mongoose est une bibliothèque qui facilite l'interaction avec les bases de données MongoDB

Nodemon est un outil utile qui permet de redémarrer automatiquement le serveur Nodejs à chaque fois que des modifications sont apportées
