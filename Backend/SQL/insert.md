# SQL

## Insert

voici la syntaxe : 

```php
$request = $database->exec('INSERT INTO tableName(email,pass) VALUES("azerty@outlook.com", "azerty")');
```

*   `$database` c'est la connection à la base de données

*   `INSERT INTO tableName(email,pass)` on insère quelque chose dans les `champs` email et pass de la table `tableName`

*   `VALUES("azerty@outlook.com", "azerty")` on dit que 'azerty@outlook.com' est égal à `email` et "azerty" à `pass`, la première valeur de `tableName` correspond à la première valeur de `VALUES`ainsi de suite.

## Requête préparée

```php
    $request = $database->prepare('INSERT INTO user(email,pass) VALUES(:email, :pass)');
    $request->bindParam(':email', $_POST['email']);
    $request->bindParam(':pass', $_POST['pass']);
    $request->execute();
```

*   `bindParam(':email', $_POST['email'])` lie :email avec $_POST[email];

*   `$request->execute()` exécute la requête préparée