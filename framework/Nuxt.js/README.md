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
```terminal
yarn create nuxt-app <project-name>
```

une fois cette commande effectué, plusieurs questions nous sont demandées : 

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

Une fois que c'est fini, il suffit de faire cd <project-name> et faire `yarn dev`.

On peut désormais accéder à l'application avec `http://localhost:3000`

note : NuxtJs surveille les modifications faites au fichier, il n'y a pas besoin de reload le server