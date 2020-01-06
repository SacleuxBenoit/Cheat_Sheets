# SQL

## Ajout d'un compte utilisateur 

Pour ajouter un compte utilisateur il faut utiliser la commande :
```
CREATE USER name_user;
```

## Suppression d'un compte utilisateur 

Pour supprimer un compte utilisateur existant il faut utiliser la commande : 
```
DROP USER name_user;
```

## Création d'une base de données 

Pour créer une base de données on utilise la commande : 
```
CREATE DATABASE name_db;
```

## Créer une database avec un propriétaire (OWNER)  

Pour créer une database avec un OWNER il faut faire la commande suivante :
```
CREATE DATABASE name_db OWNER name_user;
```

## Suppression d'une base de données 

Pour supprimer une base de données on utilise la commande : 
```
DROP DATABASE name_db;
```

## Retrouver une information dans une base de données 

Pour retrouver une information dans une base de données il faut faire : 
```
SELECT name_column FROM name_table WHERE "what we need"
```

# Database 

Pour créer une database il faut faire la commande suivante : 
```
CREATE TABLE table_name (
column_name TYPE column_constraint,
table_constraint table_constraint
);
```

Pour renommer une database il faut faire :
```
ALTER TABLE table_name RENAME TO new_table_name;
```

# Commande 

## Entrer dans une base de données 

Pour entrer dans une base de données il faut faire : 
```
\c name_db
```

## Voir les utilisateurs 

Pour voir les utilisateurs il faut faire : 
```
\du
```
## Liste des bases de données

Si nous voulons voir la liste pour les bases de données existantes ont utilise la commande : 
```
\l
```

## Quitter psql

Pour quitter PSQL il faut faire la commande : 
```
\q
```

