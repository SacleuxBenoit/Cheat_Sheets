# Step 7 - Create model

Créer un dossier `models` et un fichier `goalModel.js`

## goalModel.js

- Réalisation du model

```js
const mongoose = require('mongoose')

const goalSchema = mongoose.Schema({ // Création d'un Schéma de mongoose appelé goalSchema
    text:{
        type: String,
        required: [true, 'Please add a text value'] // Ce champ est obligatoire
    }
},{
    timestamps: true, // created_at && updated_at
})

module.exports = mongoose.model('Goal', goalSchema) // export le model
```

## goalController.js

- Importer le model Goal (ne pas oublier la majuscule)

```js
const Goal = require('../models/goalModel')
```

### Create

```js
const setGoal = asyncHandler(async (req,res) => {
    if(!req.body.text){
        req.status(400)
        throw new Error('Please add a text field')
    }

    const goal = await Goal.create({
        text: req.body.text
    })

    res.status(200).json(goal) // Affiche la réponse HTTP succès
})
```

### Read

```js
const getGoals = asyncHandler(async (req,res) => {
    const goals = await Goal.find() // Recherche tous les documents dans la collection Goal

    res.status(200).json(goals)
})
```

### Update

```js
const updateGoal = asyncHandler(async (req,res) => {
    const goal = await Goal.findById(req.params.id) // Recherche d'un goal spécifique en fonction de l'id

    if(!goal){ // Si le goal n'a pas était trouvé
        res.status(400) // Renvoie une erreur 400
        throw new Error('Goal not found')
    }

    const updatedGoal = await Goal.findByIdAndUpdate(req.params.id, req.body, { // met à jour le Goal
        new: true, // Renvoie la version mise à jour du goal
    })

    res.status(200).json(updatedGoal) // Affiche la réponse HTTP succès
})
```

### Delete

```js
const deleteGoal = asyncHandler(async (req,res) => {
    const goal = await Goal.findById(req.params.id)

    if(!goal){
        res.status(400)
        throw new Error('Goal not found')
    }

    await goal.deleteOne() // Supprime le goal de la base de données
    res.status(200).json({id: req.params.id}) // Affiche la réponse HTTP succès avec l'id du goal qui viens d'être delete
})
```