# SQL

## Ajout d'un compte utilisateur : 

Pour ajouter un compte utilisateur il faut utiliser la commande :
```
CREATE USER name_user;
```

Si nous voulons voir la liste des utilisateurs existants il faut faire la commande : 
```
\du
```
## Suppression d'un compte utilisateur :

Pour supprimer un compte utilisateur existant il faut utiliser la commande : 
```
DROP USER name_user;
```

# Base de données :

## Création d'une base de données : 

Pour créer une base de données on utilise la commande : 
```
CREATE DATABASE name_db;
```

Si nous voulons voir la liste pour les bases de données existantes ont utilise la commande : 
```
\l
```

## Suppression d'une base de données : 

Pour supprimer une base de données on utilise la commande : 
```
DROP DATABASE name_db;
```

## Retrouver une information dans une base de données : 

Pour retrouver une information dans une base de données il faut faire : 
```
SELECT name_column FROM name_table WHERE "what we need"
```

