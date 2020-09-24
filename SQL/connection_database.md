# SQL

## Se connecter à une base de données

PhP propose plusieurs moyens pour se connecter à une base de données MySQL il y a : 

*   L'extension `mysql_` cette méthode est devenue obsolète depuis la version 5.5, pour totalement disparaitre avec la V.7.0.

*   L'extension `mysqli` c'est l'abréviation de `MySQL Improved` tout comme `mysql_` cette méthode est devenue obsolète car elle n'est plus en développement actif (cette extension ne reçoit que des correctifs de sécurité).

*   L'extension `PDO` l'avantage de cette extension c'est qu'il permet d'accéder à n'importe quel type de bsae de donnéees, on peut donc l'utiliser pour ce connecter à PostgreSQL, MySQL ou encore Oracle.
 

## Se connecter avec PDO

Pour se connecter avec PDO il va nous falloir plusieurs choses : 

*   `Le nom de l'hote` nous allons travailler en local et donc utiliser `localhost`

*   `Le nom de la base de données` ici ça sera `cheatsheets`

*   `le login` c'est le login qui permet de nous identifier, par défaut c'est `root`

*   `le password` sous `WAMP` par défaut il n'y a pas de mot de passe, par contre pour `MAMP` le mot de passe par défaut est `root`

voici la synthaxe : 

```php
    Pour WAMP :
$bdd = new PDO('mysql:host=localhost;dbname=cheatsheets;charset=utf8', 'root', '');

    Et pour MAMP :
$bdd = new PDO('mysql:host=localhost;dbname=cheatsheets;charset=utf8', 'root', 'root');
```