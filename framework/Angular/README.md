## Angular

## Installation d'Angular

Pour installer Angular il suffit d'aller dans votre terminal et de faire la commande suivante : 
```
npm install -g @angular/cli
```
## Initialiser Angular

Pour initialiser Angular il faut faire : 
```
ng new my-app
```

à la place de `my-app` vous mettez bien entendu ce que vous voulez.

Une fois la commande effectué, les questions suivantes vous seront posées : 

*   Would you like to add Angular Routing ? (y/N)
*   Which stylesheet format would you like to use?
    *   Css
    *   SCSS
    *   Sass
    *   Less
    *   Stylus


## Problème avec ng

Si jamais vous rencontrez le message d'erreur : `ng: command not found` lorsque vous voulez initialiser le projet il faut aller dans votre
fichier où sont tous vos alias et mettre la commande suivante : 
```
alias ng="/Users/<user_name>/.npm-global/bin/ng"
```

il ne faut surtout pas oublier de changer le `<user_name>` par votre propre user_name, si jamais vous avez un doute il faut aller sur le terminal et faire :
`cd /Users` une fois dans le dossier Users il ne reste plus qu'a faire un `ls` et regarder le nom du dossier qui apparaît.

## Démarrer l'application

Pour démarrer l'application il suffit d'aller dans le dossier que vous venez de créer en faisant `cd my-app` et de faire `ng serve`
petit bonus : la commande `ng serve --open` permet de lancer le serveur et de directement ouvrir le localhost sur votre navigateur.


## Structure d'un projet Angular

Voici à quoi ressemble la structure : 

![alt text](images/angular-7-project-structure.png)

*   `App` Ce répertoire contient le module `AppModule` (app.module.ts), un `component` (app.component.ts), un `template` (app.component.html), le fichier `css` du template (app.component.css), le module de `navigation` (app-routing.module.ts) et le fichier de spécification du component (app.component.spec.ts).

*   `assets` Ce répertoire va contenir les contenus statiques, comme les images.

*   `environnements` Ce répertoire va permettre de définir l'environnement d'exécution (production ou développement)

*   `index.html` C'est le fichier qui héberge l'application Angular (c'est le seul fichier html).

*   `karma.conf.js` C'est le fichier de configuration pour les tests

*   `main.ts` C'est le fichier de démarrage de l'application Angular

*   `polyfills.ts` c'est un fichier pour permettre à l'application de fonctionner sur quasiment tous les navigateurs

*   `style.css` c'est le fichier global css pour l'application

*   `test.ts` c'est un fichier pour tester l'application

*   `tsconfig.app.json` c'est le fichier de configuration pour le language Typescript

*   `tsconfig.spec.json` c'est le fichier de configuration de Typescript pour les tests

*   `.editorconfig` c'est le fichier de config pour l'éditeur de code

*   `angular.json` c'est le fichier de configuration pour l'application Angular

## Notes 

Je prendrais le temps de détailler les pages plus tard