# Step 8 - User model

- Créer le fichier `userModel.js`

## userModel.js

```js
const mongoose = require('mongoose')

const userSchema = mongoose.Schema({
    name:{
        type: String,
        required: [true, 'Please add a name']
    },
    email:{
        type: String,
        required:[true, 'Please add an email'],
        unique: true // Impossible d'avoir de doublon
    },
    password:{
        type: String,
        required:[true, 'Please add password']
    }
},{
    timestamps: true // Ajout de update_at && created_at
})

module.exports = mongoose.model('User', userSchema)
```

## goalModel.js

- Add user to goal Model

```js
const mongoose = require('mongoose')

const goalSchema = mongoose.Schema({
	user:{
		type: mongoose.Schema.Types.ObjectId,
		required: true,
		ref: 'User', // fait référence au model User (utile pour les jointures)
	},
	text: {
		type: String,
		required: [true, 'Please add a text value']
	}
}, {
	timestamps: true,
})

module.exports = mongoose.model('Goal', goalSchema)
```