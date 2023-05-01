# npm

## Npm c'est quoi

Npm `Node package manager`, c'est un gestionnaire de dépendances, en gros c'est un outil qui va permettre de gérer les bibliothèques / frameworks. Depuis la version 0.6.3 il a était intégré à Nodejs c'est pour cela que quand on installe nodejs npm viens avec. 

## Comment l'installer

### Sur mac

Pour l'installer sur mac, rien de plus simple avec [Homebrew](https://brew.sh)

```bash
brew install node
```

### Sur linux

```bash
sudo apt-get install nodejs npm
```

Pour voir la version de npm il va falloir faire `npm -v`

## Commencer un projet

Pour commencer un projet, nous allons utiliser `npm init` dans le terminal plusieurs questions nous serons posés : 

*   `package name` C'est le nom du projet, si on laisse cette partie vide, le nom du dossier va être pris par défaut.

*   `version` Ici, c'est le numéro de version du projet, par défaut c'est la version 1.0.0

*   `description` C'est la description du projet, ça peut être utile si nous voulons publier le projet, la description va être référencée par npm.

*   `entry point` l'entry point c'est le fichier principal du projet, par défaut index.js (souvent renommé app.js)

*   `test command` c'est la commande qui est exécutée lorsque nous faisont `npm test` nous pouvons par exemple utilser `karma`, `jest` etc

*   `git repository` c'est l'endroit ou l'on peut trouver la source du projet

*   `keywords` mot-clé en rapport avec le projet

*   `author` nom / prénom / email de l'auteur

*   `license` ISC est la licence de base, la plupart des projets Open source Nodejs sont sous MIT

*   et enfin, il y a une demande de confirmation 

Une fois ceci fait, un fichier `package.json` va apparaître dans le dossier ou npm init a était effectué

### Package.json

dans ce fichier, on va retrouver toutes les informations que nous avons indiquées précédemment :

```json
{
  "name": "TestForcheatsheets",
  "version": "1.0.0",
  "description": "This repo is a test",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "Sacleux Benoît",
  "license": "MIT"
}

```

ce fichier est utilisé pour fournir à npm des informations qui lui permettent de gérer les dépendances du projet par exemple si nous installons `express` avec `npm install express` le package.json va être update avec la partie `dependencies` :

```json
  "dependencies": {
    "express": "^4.17.1"
  }
```