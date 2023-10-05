# Step 5 - Express Async Handler

- Installer `express-async-handler` à la racine du projet

## goalController.js

ici on va importer express-async-handler

```js
const asyncHandler = require('express-async-handler')
```

puis on va l'appeler sur tous les controllers

```js
const updateGoal = asyncHandler(async (req,res) => {
    res.status(200).json({message: `Update goal ${req.params.id}`})
})
```