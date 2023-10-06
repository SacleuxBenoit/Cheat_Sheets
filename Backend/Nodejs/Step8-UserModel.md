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
        unique: true
    },
    password:{
        type: String,
        required:[true, 'Please add password']
    }
})
```