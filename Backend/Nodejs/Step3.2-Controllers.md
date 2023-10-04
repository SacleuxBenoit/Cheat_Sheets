# Step 3.2 - Controllers

Il faut commencer par créer le dossier `controllers` et le fichier `goalController.js`

```js
const getGoals = (req, res) => { // (1)
  res.status(200).json({ message: "Get Goals" }); // (2)
};

module.exports = {
  getGoals, // (3)
};
```

## Notes

- (1) Création d'une fonction nommé getGoals qui prend 2 paramètres `req` (la demande HTTP) et `res` (la réponse HTTP)

- (2) Génération d'une réponse json pour définir le code status 200 (ok), ce qui indique que la requête a était traité avec succés, ensuite
`res.json({message: "Get Goals"})` permet d'envoyer une réponse JSON au client. La réponse contient un objet JSON avec une propriété `message` dans la valeur
et `Get Goals`

- (3) exportation de la fonction getGoals, qui est maintenant utilisable dans d'autre partie du projet (voir étape 3.1)