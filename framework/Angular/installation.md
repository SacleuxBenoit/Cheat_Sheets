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

Si jamais vous rencontrez le message d'erreur : `ng: command not found` lorsque vous voulez initialiser le projet il faut d'aller dans votre
fichier où sont tous vos alias et mettre la commande suivante : 
```
alias ng="/Users/<user_name>/.npm-global/bin/ng"
```

il ne faut surtout pas oublier de changer le `<user_name>` par votre propre user_name, si jamais vous avez un doute il faut aller sur le terminal et faire :
`cd /Users` une fois dans le dossier Users il ne reste plus qu'a faire un `ls` et regarder le nom du dossier qui apparaît.

## Démarrer l'application

Pour démarrer l'application il suffit d'aller dans le dossier que vous venez de créer en faisant `cd my-app` et de faire `ng serve`
petit bonus : la commande `ng serve --open` permet de lancer le serveur et de directement ouvrir le localhost sur votre navigateur.