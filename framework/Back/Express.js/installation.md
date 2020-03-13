## Express.js 

## Installation de Node.js

Tout d'abord il faut installer Node.js sur notre ordinateur, [Vous pouvez l'installer à cette adresse](https://nodejs.org/en/).

## Npm init

Ensuite, il va falloir créer un dossier, je vais l'appeler `test`, dans ce dossier nous allons faire un `npm init` pour créer le `package.json`, plusieurs questions vont nous être demandées : 

*   package name : (test)
*   version (1.0.0)
*   description :
*   entry point : (index.js)
*   test command : 
*   git repository
*   keywords :
*   author : 
*   license : (ISC)
*   Is this OK ? (Yes)

Pour un test, je vais faire appuyer la touche `enter` sur tout (pour prendre les paramètres par défaut) sauf pour l'entry point, je vais mettre `app.js`

## Installer express 

Nous pouvons désormais installer express, pour l'installer dans la liste des dépendances il faut faire la commande suivante : `npm install express --save`, par contre si nous voulons l'installer de façon temporaire il suffit de ne pas mettre le `--save`.

lorsque nous l'installons avec le `--save`, dans le fichier package.json 2 lignes sont rajoutées : 
  ````js
"dependencies": {
    "express": "^4.17.1"
```