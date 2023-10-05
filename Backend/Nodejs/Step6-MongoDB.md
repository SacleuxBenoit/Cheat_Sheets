# Step 6 - MongoDB

## Première étape - Création du projet

- Ce connecter sur le site MongoDB
- Créer un projet > goals app
- Button > create a deployment
- Build database > FREE > aws > Paris (EU)
- Changer le cluser name
- Créer un utilisateur
- Appuyer sur Add My Current IP Adress

## Deuxième étape

- Cliquer sur `database` dans la navBar sur la gauche
- Browse Collections > Add My Own Data
- Database name : goalsapp
- collection name : goals

## MongoDB compass

Overview > Connect > compass > I have MongoDB compass installer > copié le lien de connexion

Ouvrir le logiciel MongoDB compass et collé le lien de connexion
-> Changer `password` et le `/test` à la fin par le mot de passe et le nom de la database

Ce qui donne quelque chose comme ci-dessous

```
mongodb+srv://username:password@clusterName.b75mote.mongodb.net/goals
```

## Connection avec Mongoose

Sur le site de MongoDB :

- Connect > Drivers > copié le text

## .env

```.env
MONGO_URI = mongodb+srv://username:password@cluserName.b75mtoe.mongodb.net/goalsapp.retryWrites=true&w=majority
```

Une fois que le mot de passe / nom de la base de données et changé, il suffit de reboot le serveur

## Connection

- Il faut créer le dossier `config` avec `db.js` dedans

## db.js

```js
const mongoose = require('mongoose')
const colors = require('colors')

const connectDB = async () => {
    try{
        const connect = await mongoose.connect(process.env.MONGO_URI)
        console.log(`MongoDB Connected: ${connect.connection.host}`.cyan.underline)
    }catch(error){
        console.log(error)
        process.exit(1)
    }
}
```

## server.js

```js
const connectDB = require('./config/db')

connectDB() // En dessous des requires et au dessus de const app = express()
```