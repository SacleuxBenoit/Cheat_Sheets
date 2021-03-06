# Gitflow

## Installation

Pour installer Git-flow sur Linux il faut faire la commande suivante dans le terminal : `apt-get install git-flow`

Pour l'installer sur Mac il faut faire : `brew install git-flow`

## Initialisation

Pour initialiser git-flow dans un dépôt git il faut faire : `git flow init`

il va falloir répondre à quelques questions concernant les conventions, il est recommandé d'utiliser les valeurs par défaut.

## Passer sur une nouvelle branche basée sur la develop

Pour passer sur une nouvelle branche basée sur la develop il faut faire la commande suivante : `git flow feature start MYFEATURE`

## fusionner la branche avec la develop

Pour fusionner la branche créée avec la branche develop il faut faire : `git flow feature finish MYFEATURE`

cette commande fait :

*   fusionne la branche MYFEATURE avec la develop

*   supprime la branche MYFEATURE

*   nous fait passer sur la branche develop

## Publier une fonctionnalité 

Pour publier une fonctionnalité sur le server distant pour qu'elle puisse être utilisée par les autres utilisateurs il faut faire : 
`git flow feature publish MYFEATURE`

## Récupérer une fonctionnalité publiée 

Pour récupérer une fonctionnalité publiée par un autre utilisateur il faut faire la commande suivante :
`git flow feature pull origin MYFEATURE`

On peut aussi suivre une fonctionnalité sur le serveur distant avec : `git flow feature track MYFEATURE`

## Livraison (release)

*   Prépare la sortie d'une nouvelle version de production

*   Permets les corrections de bugs mineurs et la préparation des métadonnées de la release

## Commencer une livraison 

Pour commencer une livraison, on crée une branche basée sur la branche de développement : `git flow release start RELEASE [BASE]`

Vous pouvez si besoin ajouter le paramètre `base` le hash d'un commit à partir duquel commencera la livraison. Ce commit doit faire partie de la branche de développement.

Il est préférable de publier la branche de livraison après l'avoir créée pour permettre aux autres développeurs de commiter dessus. De la même manière que pour les fonctionnalités on utilise cette commande : `git flow release publish RELEASE`

Pour suivre une livraison sur le serveur distant il faut utiliser : 
`git flow release track RELEASE`

## Terminer une livraison

Quand on termine une livraison plusieurs actions sont réalisées : 

*   Fusionne la branche de livraison dans la branche master

*   Etiquette la livraison par son nom 

*   Fusionne la livraison dans la branche `develop`

*   Supprime la branche de livraison

la commande est : `git flow release finish RELEASE`

il ne faut pas oublier de pousser les étiquettes avec git push --tags

## Correctifs / Hotfixes

*   Les correctifs sont utiles quand il est nécessaire de corriger immédiatement l'état incorrect de la version en production.
*   Ils peuvent se baser sur l'étiquette de la branche master indiquant la version en production.

## commencer un hotfix 

Pour commencer un hotfix il faut faire : `git flow hotfix start VERSION [BASENAME]`

Le paramètre `VERSION` indique le nom de la future release corrigée. on peut spécifier si besoin quelle release s'appliquera le hotfix

## Terminer un hotfix 

quand on termine un hotfix, il est fusionné dans les branches develop et master, de plus la fusion vers master est étiquetée par la version du hotfix. Il faut faire la commande `git flow hotfix finish VERSION `

## Supprimer complètement une branche au sein d'un dépôt git

Pour supprimer complètement une branche il faut la supprimer en locale et sur le dépôt distant.

Pour supprimer la branche qui est en locale il faut faire :
```bash
git branch -d [Nom_de_la_branche]
```

Cette commande va afficher un avertissement si la branche n'a pas été totalement fusionnée avec le répertoire principal du dépôt. Pour passer outre on utilise :
```bash
git branch -D [Nom_de_la_branche]
```

Pour supprimer la branche située sur le dépôt distant, il faut faire : 
```bash
git push [nom_du_dépot_distant] : [Nom_de_la_branche]
```

Si ont à utilisé git clone pour créer la branche, celle-ci attribue par défaut le nom origin au dépôt distant. la commande devient :
```bash
git push origin : [Nom_de_la_branche]
```

Si on utilise une version de git plus récente, la syntaxe de la commande a était simplifiée : 
```bash
git push origin --delete [Nom_de_la_branche]
```

Une fois cette commande effectuée, il faut faire la commande suivante sur tous les autres ordinateurs afin de propager le changement : 

```bash
 git fetch --all --prune
```