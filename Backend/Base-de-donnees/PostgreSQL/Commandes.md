# PostgreSQL

## Ajout d'un compte utilisateur 

Pour ajouter un compte utilisateur on va devoir utiliser `CREATE USER` :

```psql
CREATE USER name_user;
```

## Suppression d'un compte utilisateur 

Pour supprimer un compte utilisateur existant il va falloir utiliser la commande `DROP USER`

```psql
DROP USER name_user;
```

## Création d'une base de données 

on va pouvoir créer une base de données avec la commande `CREATE DATABASE`

```psql
CREATE DATABASE name_db;
```

## Créer une database avec un propriétaire (OWNER)  

Si l'on veut créer une base de données avec un propriétaire spécifique il va falloir utiliser `OWNER`

```psql
CREATE DATABASE name_db OWNER name_user;
```

## Suppression d'une base de données 

Pour supprimer une base de données c'est assez facile (un peu trop même) on utilise `DROP DATABASE` 

```psql
DROP DATABASE name_db;
```

## Retrouver une information dans une base de données 

Pour retrouver une information dans une base de données il faut faire : 

```psql
SELECT name_column FROM name_table WHERE "what we need"
```

## Database 

Pour créer une table il faut faire la commande suivante : 
```psql
CREATE TABLE table_name (
column_name TYPE column_constraint,
table_constraint table_constraint
);
```

Si nous voulons modifier une table on va devoir utilser `ALTER TABLE`, on va pouvoir ajouter/supprimer des columnes, rename la table, changer de propriétaire et bien plus encore ...

```psql
ALTER TABLE table_name RENAME TO new_table_name;
```

## Commandes

## Entrer dans une base de données 

Pour entrer dans une base de données il faut utiliser : 

```psql
\c name_db
```

## Voir les utilisateurs 

Pour voir les utilisateurs il faut faire : 

```psql
\du
```
## Liste des bases de données

Si nous voulons voir la liste pour les bases de données existantes ont va utiliser la commande : 

```psql
\l
```

## Quitter psql

Pour quitter PSQL rien de plus simple :

```psql
\q
```