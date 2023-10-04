# Step 3.1 - Routes

Pour commencer, il va falloir créer le dossier `routes` et le fichier `goalRoutes.js` dans le dossier backend

## goalRoutes.js

- Initialiser `express` et `express.Router`
- Import de `getGoals` du dossier controllers (création de ce dossier dans la prochaine étape)
- ajout de la `route` pour le getGoals
- Exporter `router`

```js
const express = require("express");
const router = express.Router();
const { getGoals } = require("../controllers/goalControllers"); // Création de ce fichier dans l'étape 3.2 - Controllers

router.get("/", getGoals); // Création de ce controller dans la prochaine étape

module.exports = router;
```
