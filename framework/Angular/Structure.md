## Angular 

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