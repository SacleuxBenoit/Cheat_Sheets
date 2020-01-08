# Framework

## C'est quoi NuxtJs

NuxtJs est un framework basé sur Vue.js, il permet de faire du SSR (server side Rendering)

il viens avec c'est package : 

*   Vue
*   Vue router 
*   Vuex
*   Vue Server Renderer
*   [Vue meta](https://www.npmjs.com/package/vue-meta) 

## Installation de Nuxt.js

Pour installer Nuxt.js il faut faire la commande suivante :
```
yarn create nuxt-app <project-name>
```

une fois cette commande effectué, plusieurs questions nous sont demandés : 

*   Project name
*   Project description
*   Author name 
*   Choose the package manager (yarn ou npm)
*   Choose UI framework 
*   Choose custom server framework 
*   Choose nuxtjs modules
*   Choose linting tools
*   Choose test framework
*   Choose rendering mode

Une fois que c'est finit, il suffit de faire cd <project-name> et faire `yarn dev`.

On peut désormais accéder à l'application avec `http://localhost:3000`

note : NuxtJs surveille les modifications faites au fichier, il n'y a pas besoin de reload le server

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

# configuration 

## Build

Cette option permet de configurer différents paramètres pour l'étape de `build`, incluant les `loaders`, `filenames` et la configuaration de `webpack` et de `transpilation

## css

Cette option nous permet de définir les fichiers css, modules et bibliothèques que nous voulons inclure en global

## dev 

Cette option nous permet de définir le mode `development` ou le mode `production`.

## env

Cette option nous permet de définir des variables d'environnement disponnible côté client et côté serveur.

## generate 

Cette option nous permet de définir chaque paramètre pour chaque route dynamique de notre application qui sera transformée en fichier HTML par nuxt.js 

## head 

Cette option nous permet de définir les balises meta par défaut de notre application 

## loading 

Cette option nous permet de personnaliser le composant de chargement par défaut chargé par nuxt.js

## modules

Cette option nous permet d'ajouter des modules Nuxt à notre projet

## modulesDir 

Cette option nous permet de définir le répertoir node_modules de notre application Nuxt.js

## plugins

Cette option nous permet de définir des plugins JavaScript qui seront exécutés avant d'instancier la racine de l'application Vue.js

## rootDir 

Cette option nous permet de définir l'espace de travail de notre application Nuxt.js

## router

Avec l'option `router`, on modifie la configuration Nuxt.js par défaut de vue router

## server

Cette option nous permet de configurer les variables de connexion à l'instance du serveur de notre application Nuxt.js

## dir 

cette option nous permet de définir les répertoires personnalisés de notre application Nuxt.js

## transition 

Cette option nous permet de définir les propriétés par défaut des transitions de pages.