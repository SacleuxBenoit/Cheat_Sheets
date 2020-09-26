# SQL

## Insert

voici la syntaxe : 

```php
$database = $request->exec('INSERT INTO tableName(email,pass) VALUES("azerty@outlook.com", "azerty")');
```

*   `$database` c'est la connection à la base de données

*   `INSERT INTO tableName(email,pass)` on insère quelque chose dans les `champs` email et pass de la table `tableName`

*   `VALUES("azerty@outlook.com", "azerty")` on dit que 'azerty@outlook.com' est égal à `email` et "azerty" à `pass`.