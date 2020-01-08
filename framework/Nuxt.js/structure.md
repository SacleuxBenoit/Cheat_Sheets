# Structure des répértoires 

## Le répértoire assets

Le répértoire assets contient des ressources NON compilés, tels que des fichiers stylus ou sass, même des images et des polices.

## Le répértoire components 

Le répertoire components contient les composants vue.js, on ne peut pas utiliser les méthodes `asyncData` ou `fetch`

## Le répertoire Layouts 

Le répertoire Layouts contient les mises en page des applications, les mises en pages sont utilisées pour changer l'aspect de la page 

note : ce répertoire ne peut pas être rennomé sans configuration supplémentaires 

## Le répertoire des middlewares

Le répertoire middlewares contient les middleswares, il permet de définir une fonction qui sera éxecuté avant de faire le rendu d'une mise en page, ou d'un groupe de mise en page.

## Le répertoire des pages

ce répertoire contient les vues et les routes d'application, le framework lit tous les fichers en `.vue` dans ce répertoire et crée automatiquement le routage de l'application

note : ce répertoire ne peut pas être rennomé sans configuration supplémentaires.

## Le répertoire plugins

Le répertoire plugin contient les plugins JavaScript que l'ont souhaite exécuter avant d'instancier l'application vue.js racine, c'est l'endroit pour mettre les composants globaux et injecté des fonctions ou constantes.

## Le répertoire statics

Le répertoire static est directement relié au chemin racine du serveur (/static/test.txt est accessible à l'adresse http://localhost:3000/test.txt) et contient des fichiers que l'on ne veut pas modifier (par ex. le favicon)

note : ce répertoire ne peut pas être rennomé sans configuration supplémentaires.

## Le répertoire des stores

ce répertoire contient les fichiers ce store vuex. les stores vuex sont implémenté de manière optionnelle dans le framework Nuxt.js. La création d'`index.js` dans ce répertoire active automatiquement l'option dans le framework

note : ce répertoire ne peut pas être rennomé sans configuration supplémentaires.

## le fichier nuxt.config.js 

ce fichier contient les configurations personnalisée concernant Nuxt.js

## le fichier package.json

le fichier package.json contient les dépendances et scripts de l'application

note : ce fichier ne peut pas être rennomé 