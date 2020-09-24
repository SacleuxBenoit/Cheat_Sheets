# SQL

## Se connecter à une base de données

PhP propose plusieurs moyens pour se connecter à une base de données MySQL il y a : 

*   L'extension `mysql_` cette méthode est devenue obsolète depuis la version 5.5, pour totalement disparaitre avec la V.7.0.

*   L'extension `mysqli` c'est l'abréviation de `MySQL Improved` tout comme `mysql_` cette méthode est devenue obsolète car elle n'est plus en développement actif (cette extension ne reçoit que des correctifs de sécurité).

*   L'extension `PDO` l'avantage de cette extension c'est qu'il permet d'accéder à n'importe quel type de bsae de donnéees, on peut donc l'utiliser pour ce connecter à PostgreSQL, MySQL ou encore Oracle.
 