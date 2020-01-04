# SQL

## !!! Cheat_sheets en cours de développement !!! :

note : 
 
* n = la taille

* d = le nombre de chiffre après la virgule

## Les données de type texte

`CHAR(n)` Peut contenir une chaine de caractère, elle peut contenir jusqu'à 255 caractères

`VARCHAR(n)` Peut contenir une chaine de caractère qui possède une taille variable, elle peut contenir jusqu'à 255 caractères

`TEXT` Peut contenir une chaine de caractère de moins de 65 535 caractères

`TINYTEXT` Peut contenir une chaine de caractère de moins de 255 caractères

`MEDIUMTEXT` Peut contenir une chaine de caractère de moins de 16 777 215 caractères

`LONGTEXT` Peut contenir une chaine de caractère de moins de 4 294 967 295 caractères

`ENUM` Peut contenir une liste de données, la liste peut contenir jusqu'à 65 535 données.

## Les données de type nombre

`INT(n)` Peut contenir un nombre entre -2 147 483 648 et 2 147 483 647 

`TINYINT(n)` Peut contenir un nombre entre -128 et 127

`SMALLINT(n)` Peut contenir un nombre entre -32 768 et 32 767

`MEDIUMINT` Peut contenir un nombre entre -8 388 608 et 8 388 607

`BIGINT` Peut contenir un nombre entre -9 223 372 036 854 775 808 et 9 223 372 036 854 775 807

`FLOAT(n,d)` Peut contenir un petit nombre à virgule flottante

`DOUBLE(n,d)` Peut contenir un grand nombre à virgule flottante

`DECIMAL(n,d)` Peut contenir un type `DOUBLE(n,d)`, mais sous forme d'une chaine de caractère

