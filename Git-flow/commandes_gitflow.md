# Gitflow

## Installation

Pour installer Git-flow sur linux il faut faire la commande suivante dans le terminal : `apt-get install git-flow`

## Initialisation

Pour initialiser git-flow dans un dépôt git il faut faire : `git flow init`

il va falloir répondre à quelques questions concernant les conventions, il est recommandé d'utiliser les valeurs par défaut.

## Passer sur une nouvelle branche basé sur la develop

Pour passer sur une nouvelle branche basé sur la develop il faut faire la commande suivante : `git flow feature start MYFEATURE`

## fusionner la branche avec la develop

Pour fusionner la branche créer avec la branch develop il faut faire : `git flow feature finish MYFEATURE`

cette commande fait :

* fusionne la branche MYFEATURE avec la develop

* supprime la branche MYFEATURE

* nous fait passer sur la branch develop

