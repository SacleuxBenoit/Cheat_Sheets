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

## Problème avec ng

Si jamais vous rencontrez le message d'erreur : `ng: command not found` lorsque vous voulez initialiser le projet il faut d'aller dans votre
fichier ou sont tous vos aliass et mettre la commande suivant : 
```
alias ng="/Users/<user_name>/.npm-global/bin/ng"
```

il ne faut surtout pas oublier de changer le `<user_name>` par votre propre user_name, si jamais vous avez un doute sur votre terminal il faut faire :
`cd /Users` une fois dans le dossier Users il ne reste plus qu'a faire un `ls` et regarder le nom du dossier qui apparait.