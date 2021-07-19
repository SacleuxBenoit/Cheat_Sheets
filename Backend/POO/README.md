## Syntaxe d'une classe

Il faut utiliser le mot clé `class` suivi du nom de la classe

```php
<?php
class Personnage{
// déclaration des attributs et méthodes ici
}
?>
```

il faut savoir que pour respecter la notation PEAR le nom de la classe commence par une majuscule.

## Visibilité d'un attribut ou d'une méthode

la visibilité d'un attribut ou d'une méthode nous indique à partir d'ou on peut y avoir accès :
il existe 2 types : `private` && `public`.

*   `public` on peut y accéder depuis n'importe ou.

*   `private` ici, nous pouvons avoir accès aux attributs et méthode UNIQUEMENT à l'interieur de la classe.

## Création d'un attribut

voici la syntaxe d'un attribut :

```php
class Personnage{
    private $_life = 100;
    private $_mana = 50;
}
```

on utilise le mot-clé private suivi du nom de l'attribut (avec un underscore au début, c'est la notation PEAR) puis la valeur de l'attribut.

## Création d'une méthode 

```php
class Personnage{
    private $_life = 100;
    private $_mana = 50;

    public function move(){
        // une méthode qui permet de déplacer le personnage
    }
}
```

il faut mettre la visibilité `public` ou `private` (en général la visibilité est public), ensuite utiliser `function` puis mettre le nom de la fonction.

## Définition

*   `attribut` un attribut désigne une variable.

*   `méthode` une méthode désigne une fonction.