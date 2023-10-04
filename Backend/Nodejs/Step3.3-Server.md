# Step 3.3 - Server

il reste maintenant plus qu'à configurer la route : 

```js
app.use("/api/goals", require('./routes/goalRoutes')) // (1)
```

- `app` c'est l'instance d'express
- `.use()` c'est une méthode d'express qui permet d'utiliser des middlewares / des routes
- `"/api/goals", require('./routes/goalRoutes')` signifie que toutes les routes définis dans goalRoutes seront préfixées par `/api/goals`