# Initialisation

`symfony new --webapp --version=lts project_name`

cette commande va nous permettre d'initialiser le projet

*   L'option `--webapp` installe tous les packages nécessaires pour créer des applications web.

*   L'option `--version=lts` prend en compte la dernière version stable (lts pour long-term support).

<!-- ## Installation des outils et certificats

*   `sudo apt install libnss3-tools`

*   `symfony server:ca:install` -->

## Lancement du serveur symfony 

*   `symfony serve`

## Création de la database avec les install scripts

*   Cloner `https://github.com/jibundeyare/install-scripts`

*   Dans le terminal utiliser la commande suivante : `./mkdb.sh project_name`

## Création de la database avec PhpMyAdmin

*   Créer un user : Compte utilisateurs > Ajouter un compte d'utilisateur

*   Cocher la case `Créer une base portant son nom et donner à cet utilisateur tous les privilèges sur cette base. `

## création du fichier .env.local

*   il faut commencer par créer un fichier `.env.local` à la racine du projet.

*   ensuite il faut aller dans le fichier `.env` et copier la ligne `DATABASE_URL="mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=5.7&charset=utf8mb4"`.

*   puis l'insérer dans le fichier .env.local (sans le `#` au début de la ligne).

une fois ceci fait, il va falloir modifier quelques éléments :

*   `db_user` le nom de l'utilisateur.

*   `db_password` le mot de passe de la bdd.

*   `db_name` par le nom de la base de données.

*   `server_version=...` par la version actuelle de la base de données

au final cela va donner quelque chose comme :

`DATABASE_URL="mysql://project_name:42@127.0.0.1:3306/project_name?serverVersion=&charset=utf8mb4"`

## Création des classes

`php bin/console make:entity`

une série de questions va nous être posée : 

*   `Class name of the entity to create or update` tout simplement le nom de la classe (avec une majuscule au début) 2 fichiers vont donc être créés par exemple pour la class Product : 
`src/Entity/Product.php` && `src/Repository/ProductRepository.php`

*   `New property name`

*   `field type` ici il faut préciser le type : booléan / string / int / datetime etc

*   `field length` par défaut la taille est de 255 mais la convention veut que pour un titre ou un mot de passe on utilise 191

*   `can this field be null in the database` choix par défaut : no `src/Entity/Product.php` va être update

*   `Add another property` il suffit d'appuyer sur la touche Enter pour dire non si nous n'avons pas d'autres propriétés à ajouter

## Migration des tables / schémas de la base de données

pour ce faire nous allons utiliser la commande `php/bin console make:migration` si tout à fonctionner on devrait avoir un message comme : 

```bash
SUCCESS!

Next: Review the new migration "migrations/Version20211116204726.php"
Then: Run the migration with php bin/console doctrine:migrations:migrate
```

Ensuite il faut utiliser la commande : `php bin/console doctrine:migrations:migrate` ou son alias : `php bin/console do:mi:mi`, cette commande exécute tous les fichiers de migrations
qui n'ont pas encore été exécutés sur la base de données.