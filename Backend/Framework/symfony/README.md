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

## Créer les relations entre tables

Pour avoir une relation `ManyToOne` entre `Livre` et `Auteur` :

*   Dans le terminal : `php bin/console make:entity`

*   Renseigner la classe que l'on veut modifier donc ici `Livre`

*   ` New property name (press <return> to stop adding fields)` ici il faut indiquer `auteur` ATTENTION il n'y a pas de majuscule

*   `Field type (enter ? to see all types)` c'est ici qu'il faut préciser `ManyToOne`

*   `What class should this entity be related to?` ça va être `Auteur`

*   `Is the Livre.auteur property allowed to be null (nullable)? (yes/no) [yes]:` il faut ce poser la question : un livre doit-il obligatoirement avoir un auteur ? si la réponse est oui : écrire `no`

*   `Do you want to add a new property to Auteur so that you can access/update Livre objects from it - e.g. $auteur->getLivres()? (yes/no) [yes]:`

*   `New field name inside Auteur [livres]:`

et voilà !

## Créer des données de test brut

*   Pour commencer il faut faire `composer require --dev orm-fixtures` pour installer les fixtures.

*   Ensuite `symfony console make:fixtures TestFixtures` pour créer le fichier `TestFixtures`.

Une fois le fichier créé il est maintenant possible de créer des données de test

*   Créer une fonction `loadUser` dans la classe `TestFixtures` avec comme paramètre `ObjectManager $manager`

*   Ajouter un tableau avec les données brut :

```php
$userDatas = [
    [
        "email" => "admin@example.com",
        "roles" => "ROLE_ADMIN",
        "password" => "2y/H2ChUxriH.0Q33g3EUEx.S2s4j/rGJH2G88jK9nCP60GbUW8mi5K",
        "enabled" => true,
        "created_at" => DateTimeImmutable::createFromFormat('Y-m-d H:i:s', '2020-01-01 09:00:00'),
        "updated_at" => DateTimeImmutable::createFromFormat('Y-m-d H:i:s', '2020-01-01 09:00:00'),
    ],
    [
        "email" => "foo.foo@example.com",
        "roles" => "ROLE_EMRUNTEUR",
        "password" => "2y/H2ChUxriH.0Q33g3EUEx.S2s4j/rGJH2G88jK9nCP60GbUW8mi5K",
        "enabled" => true,
        "created_at" => DateTimeImmutable::createFromFormat('Y-m-d H:i:s', '2020-01-01 10:00:00'),
        "updated_at" => DateTimeImmutable::createFromFormat('Y-m-d H:i:s', '2020-01-01 10:00:00'),
    ]
]
```

*   Ensuite il va falloir utiliser une boucle foreach

```php
foreach ($userDatas as $userData){
    $user = new User();
    $user->setRoles($userData['roles']);
    $user->setEmail($userData['email']);
    $user->setPassword($userData['password']);
    $user->setEnabled($userData['enabled']);
    $user->setCreatedAt($userData['created_at']);
    $user->setUpdatedAt($userData['updated_at']);

    $manager->persist($user);
}
```

*   Il ne reste plus qu'à mettre `$this->loadUser($manager);` dans la fonction `load()`

*   Puis finir avec la commande `php bin/console doctrine:fixtures:load` dans le terminal.


# Notes

*   Symfony viens avec le package `symfony/maker-bundle`, pour nous aider à trouver toutes les commandes il faut faire
`symfony console list make`