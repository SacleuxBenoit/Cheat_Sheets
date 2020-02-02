# Terminal

## CD

Pour naviguer dans un répertoire on utilise la commande `cd` succédée du nom du répertoire.

`cd /` Permet de se retrouver à la racine du site.

`cd ~` ou `cd` Permet d'accéder au répertoire de l'utilisateur.

`cd sites/prod` permet d'aller dans le répertoire prod.

`cd ..` Remonte dans le répertoire parent à partir de l'endroit ou vous avez utilisé cette commande.

`cd -` Permet de revenir au répertoire précédent.

`pwd` Renvoie le chemin absolu du répertoire.

## LS

La commande `ls` permet de lister le contenu du répertoire

`ls -a` Affiche les fichiers cachés.

`ls -l` Affiche les informations de manière détaillée.

`ls -la` Affiche tous les fichiers, même les fichiers cachés.

`ls /etc/` Affiche le contenu du répertoire /etc/

`ls -r` Tri de façon inversé.

`ls -t` Tri les fichiers du plus récent au plus ancien.

`ls -S` Tri par taille décroissante.

`ls -lhS` Affiche les informations des fichiers, avec les tailles et ordonnée du plus grand au plus petit.

`ls -i` Affiche le numéro d'inode, il est unique à chaque dossier de votre systeme de fichier.

## Autres

`man` Permet d'afficher le manuel d'aide de n'importe quelle commande par exemple `man ls` affiche le manuel d'aide de la commande ls

`head` Permet d'afficher le début d'un fichier (par défaut elle affiche les 10 premières lignes). Par exemple `head README.md` ça affiche les 10 premières ligne du readme.

`tail` Fait le contraire de `head` cette commande permet d'afficher la fin d'un fichier (par défaut elle affiche les 10 dernières lignes). Par exemple `tail README.md` ça affiche les 10 dernières ligne du readme.

 `wc Linux_commandes` Affiche le nombre de ligne + mots + caractères du fichier Linux_commandes.

 `date` Affiche la date, le mois, l'heure et l'année.

`!!` Exécute la dernière commande utilisée dans le terminal.

`cat` Affiche le fichier texte dans le terminal.

`less` Simillaire à `cat` mais affiche le fichier page par page.

`touch inxdex.html` Crée un fichier index.html

`mkdir projet` Crée un dossier projet. 

`cp` Fait une copie d'un fichier, l'option `-R` permet des copies de dossiers entiers.

`rm` Supprime des fichiers, l'option `-f` force la suppression, l'option `-i` demande une confirmation avant la suppression et l'option `-r` permet de supprimer les dossiers.

`echo "ceci est un test"` Affiche `ceci est un test` sur la console.

Quelque cas pratique de `echo` : 

-> `echo "ceci est un test" >> monfichier` grâce au signe `>>`, ça va écrire le texte à la fin du fichier `monficher` sans en écraser le contenu

-> `echo "ceci est un test" > monfichier` Par contre pour écraser un fichier, en effaçant tout son contenu, on utilise le signe `>`.

`uptime` La principale fonction de la commande `uptime` c'est d'indiquer depuis combien de temps le système fonctionne, 
cette commande affiche : 
*   l'heure actuelle
*   le temps depuis lequel le system est en marche
*   le nombre d'utilisateurs de connectés 
*   et la charge du system