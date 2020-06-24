# PostgreSQL

## Installation sur Mac

Pour installer Postgresql en ligne de commande avec Homebrew, on va utiliser :

```bash
brew install postgresql
```

La commande ci-dessous va nous permettre de lancer postgre automatiquement au démarrage du Mac

```bash
brew services start postgresql
```

## Installation sur Linux

Pour l'installer sur Linux il suffit de faire la commande ci-dessous 

```bash
sudo apt install postgresql
```

## Première utilisation

Pour la première utilisation il va falloir suivre les étapes suivantes :

*   écrire `psql postgres` dans le terminal

*   Nous allons créer un premier rôle `User` avec un mot de passe `CREATE ROLE User WITH LOGIN PASSWORD 'yourpassword';`

*   Ensuite, il va falloir lui donner la permission de créer une base de données `ALTER ROLE User CREATEDB`

*   Une fois ceci fait, on peut maintenant quitter avec `\q`

*   Nous pouvons maintenant nous connecter à notre nouvel utilisateur en faisant `psql postgre -U User`

*   Une fois connecté nous allons créer notre première base de données `CREATE DATABASE nameOfTheDatabase;`