# SQL

## Se connecter à une base de données

PhP propose plusieurs moyens pour se connecter à une base de données MySQL il y a : 

*   L'extension `mysql_` : cette méthode est devenue obsolète depuis la version 5.5, pour totalement disparaitre avec la V.7.0.

*   L'extension `mysqli` : c'est l'abréviation de `MySQL Improved` tout comme `mysql_` cette méthode est devenue obsolète car elle n'est plus en développement actif (cette extension ne reçoit que des correctifs de sécurité).

*   L'extension `PDO` : l'avantage de cette extension c'est qu'il permet d'accéder à n'importe quel type de bsae de donnéees, on peut donc l'utiliser pour ce connecter à PostgreSQL, MySQL ou encore Oracle.
 

## Se connecter avec PDO

Pour se connecter avec PDO il va falloir plusieurs choses : 

*   `Le nom de l'hôte` nous allons travailler en local et donc utiliser `localhost`

*   `Le nom de la base de données` ici ça sera `cheatsheets`

*   `le login` c'est le login qui permet de nous identifier, par défaut c'est `root`

*   `le password` sous `WAMP` par défaut il n'y a pas de mot de passe, par contre pour `MAMP` le mot de passe par défaut est `root`

voici la syntaxe : 

```php
    Pour WAMP :
$database = new PDO('mysql:host=localhost;dbname=cheatsheets;charset=utf8', 'root', '');

    Et pour MAMP :
$database = new PDO('mysql:host=localhost;dbname=cheatsheets;charset=utf8', 'root', 'root');
```

pour le moment tout est en local, mais lorsque le site sera en ligne le nom de l'hôte, le login ou encore le password vont surement changer.

### Voir la présence d'une erreur

```php

try
{
    $database = new PDO('mysql:host=localhost;dbname=cheatsheets;charset=utf8', 'root', '');
}
catch (Exception $e)
{
    die('Erreur : ' . $e->getMessage());
}
```

Ici php exécute le code dans le `try` si une erreur survient, il exécute le `catch` en arrêtant l'exécution de la page et en affichant un message pour décrire l'erreur, s'il n'y a pas de problème, php exécute uniquement la partie `try`.