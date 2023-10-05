# Step 4 - Body data & Exception Handling

## Server.js

```js
app.use(express.json())
app.use(express.urlencoded({extended: false}))
```

La première ligne configure Express pour analyser les données JSON envoyée dans le corp des requêtes HTTP, cette ligne permet de convertir automatiquement le JSON en un objet javascript.

La deuxième ligne configure Express pour analyser les données envoyées dans le corps des requêtes HTTP avec le format `application/x-www-form-urlencoded`

## goalController.js

```js
const setGoal = (req,res) => {
    console.log(req.body)
    res.status(200).json({message: "Create goal"})
}
```

## Postman

Aller sur la requête POST > body > `form-encode`

```
name = first name text
value = first value text
```

puis regarder dans la console.

## goalController.js

```js
const setGoal = (req,res) => {
    if(!req.body.text){
        res.status(400)
        throw new Error('Please add a text field)
    }
    res.status(200).json({message: "Create goal})
}
```

On définis une fonction `setGoal` qui prend deux paramètres : `req` et `res`

Ensuite on vérifie si la propriété `text` est absente / vide dans le corps de la requête `req.body`

Si la condition est vrai c'est qu'il n'y a pas de champ text / qu'il est vide, donc on renvoi une erreur 400 avec comme message `Please add a text field`

Si la condition est fausse, renvoi un status 200 ainsi qu'un objet JSON avec comme message "Ceate goal"

# Middleware

Créer un dossier `middleware` et un fichier errorMiddleware.js (dans le dossier précedemment créé)

## errorMiddleware.js

```js
const errorHandler = (err,req,res,next) => {
    const statusCode = res.statusCode ? res.statusCode : 500
    res.status(statusCode)

    res.json({
        message: err.message,
        stacl: process.env.NODE_ENV === 'production' ? null : err.stack
    })
}

module.exports = {
    errorHandler
}
```

Ce code définit un gestionnaire d'erreurs qui se produit pendant le traitement des reqiêtes HTTP et renvoie une erreur appropriées