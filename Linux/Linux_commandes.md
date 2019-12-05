# Linux

## CD

Pour naviguer dans un répértoire on utilise la commande `cd` succédée du nom du répértoire.

`cd /` Permet de se retrouver à la racine du site.

`cd ~` ou `cd` Permet d'accéder au répértoire de l'utilisateur.

`cd sites/prod` permet d'aller dans le répértoire prod.

`cd ..` Remonte dans le répértoire parent à partir de l'endroit ou vous avez utilisé cette commande.

`cd -` Permet de revenir au répértoire précédent.

`pwd` Renvoie le chemin absolu du répértoire.

## LS

La commande `ls` permet de lister le contenu du répértoire

`ls -a` Affiche les fichiers cachés.

`ls -l` Affiche les informations de manière détaillée.

`ls -la` Affiche tous les fichiers, même les fichiers cachés.

`ls -r` Tri de façon inversé.

`ls -t` Tri les fichiers du plus récent au plus ancien.

`ls -S` Tri par taille décroissante.

`ls -lhS` Affiche les informations des fichiers, avec les tailles et ordonnée du plus grand au plus petit.

`ls -i` Affiche le numéro d'inode, il est unique à chaque dossier de votre systeme de ficher.


## Autres

`man` Permet d'afficher le manuel d'aide de n'importe quelle commande par exemple `man ls` affiche le manuel d'aide de la commande ls

`head` Permet d'afficher le début d'un fichier (par défaut elle affiche les 10 premières lignes). Par exemple `head README.md` ça affiche les 10 premières ligne du readme.

`tail` Fait le contraire de `head` cette commande permet d'afficher la fin d'un fichier (par défaut elle affiche les 10 dernières lignes). Par exemple `tail README.md` ça affiche les 10 dernières ligne du readme.

