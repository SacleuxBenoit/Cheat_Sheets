# Step 1 - init project

## Initialisation des dossiers

- Création du fichier <span style="color:#ffff00">.gitignore</span>
- Ajout de <span style="color:#ffff00">node_modules</span> et de <span style="color:#ffff00">.env</span> dans le .gitignore

- Création du dossier <span style="color:#ffff00">backend</span>, puis <span style="color:#ffff00">server.js</span> dans ce même-dossier
  - server.js : `console.log("Hello World)`

## Racine du projet

- npm init > changer l'entry point en <span style="color:#ffff00">server.js</span>
- npm i express dotenv<span style="color:#00b0f0">(1)</span> mongoose<span style="color:#00b0f0">(2)</span> colors
- npm i -D nodemon<span style="color:#00b0f0">(3)</span>

## Package.json

```json
"scripts":{
    "start": "node backend/server.js",
    "dev": "nodemon backend/server.js"
}
```

Il suffit maintenant de faire un <span style="color:#ffff00">npm run server</span> dans le terminal pour faire apparaître le `Hello World`

# Notes

<span style="color:#00b0f0">(1)</span> Le module <span style="color:#00ffe1">dotenv</span> est utile pour gérer les variables d'environnement, il permet de stocker des configurations sensible, telles que des clés d'API, des identifiants de base de données, des token d'authentication etc

<span style="color:#00b0f0">(2)</span><span style="color:#00ffe1"> Mongoose</span> est une bibliothèque qui facilite l'interaction avec les bases de données MongoDB

<span style="color:#00b0f0">(3)</span><span style="color:#00ffe1"> Nodemon</span> est un outil utile qui permet de redémarrer automatiquement le serveur Nodejs à chaque fois que des modifications sont apportées
