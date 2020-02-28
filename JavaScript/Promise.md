# Javascript

## Promise

La `Promise` est utilisée pour réaliser des traitements de données de façon asynchrone (on lance un traitement, on continue d’exécuter notre programme puis une fois que le traitement est terminé on revient dessus et on peut exploiter les résultats obtenus.)

*   Un "code producteur" qui fait quelque chose et qui prend du temps. par exemple : du code qui charge les données sur un réseau.

 *   un "code consommateur" qui veut le résultat du "code producteur" une fois prêt. Beaucoup de fonctions peuvent avoir besoin de ce résultat.

 *   Une `Promise` est un objet Javascript spécial qui relie le "code producteur" et le "code consommateur". Le "code producteur" prend le temps dont il a besoin pour produire le résultat promis, et la `Promise` mais ce résultat à disposition de tout le code souscrit lorsqu'il est prêt.

 voici la syntaxe du constructeur pour un objet `Promise` : 

 ```
 let promise = new Promise(function(resolve, reject) {
   // executor (the producing code)
 });
 ```

 La fonction après new Promise est appelée exécuteur. Quand une nouvelle promise est créée, l'exécuteur s'exécute automatiquement. Il contient le "code producteur" qui devrait éventuellement produire le résultat.

 Ses arguments `resolve` et `reject` sont des rappels fournis par Javascript. Notre code est uniquement à l'intérieur de l'exécuteur.

Lorsque l'exécuteur obtient le résultat, que ce soit tôt ou tard, peu importe, il doit appeler l'un de ces rappels:

*   `resolve(value)` si le travail est fini avec succès, avec comme résultat `value`

*   `reject(error)` si une erreur se produit, `error` est l'objet d'erreur.

Donc pour résumer : l'exécuteur s'exécute automatiquement et tente d'effectuer un travail, une fois la tentative terminée, il appelle `resolve` si elle réussit
ou `reject` en cas d'erreur.

L'objet `promise` retourné par le constructeur `new promise` à ces propriétés interne : 

*   `state` initialement `pending`, puis `fulfilled` quand `resolve` est appelé ou `reject` quand reject est appelé

*   `result` initialement `undefined`, puis passe à `value` quand `resolve(value)` est appelé ou `error` quand `reject(error)` est appelé.

Voice un exemple de constructeur promise et d'une simple fonction exécuteur avec un code qui prend du temps : 

```
let promise = new Promise(function(resolve, reject) {
  // the function is executed automatically when the promise is constructed

  // after 1 second signal that the job is done with the result "done"
  setTimeout(() => resolve("done"), 2000);
});
```

Nous pouvons voir 2 chose en lancant le code au dessus : 

*   l'exécuteur est appelé automatiquement et immdédiatement par `new Promise`

*   l'exécuteur reçoit 2 arguments `resolve` et `reject`. Ces fonctions sont prédéfinis par le moteur Javascript, nous n'avons donc pas besoin de les créer. Nous devons appelé l'un deux une fois prêt.

Après 2 secondes de traitement l'exécuteur appele `resolve("done")` pour produire le résultat cela change l'état de l'objet de promise.


