# Javascript

## Promise

La `Promise` est utilisée pour réaliser des traitements de données de façon asynchrone (on lance un traitement, on continu d’exécuter notre programme puis une fois que le traitement est terminé on revient dessus et on peut exploiter les résultats obtenus.)

*   Un "code producteur" qui fait quelque chose et qui prend du temps. par exemple : du code qui charge les données sur un réseau.

 *   un "code consommateur" qui veut le résultat du "code producteur" une fois prêt. Beaucoup de fonctions peuvent avoir besoin de ce résultat.

 *   Une `Promise` est un objet Javascript spécial qui relie le "code producteur" et le "code consommateur". Le "code producteur" prend le temps dont il a besoin pour produire le résultat promis, et la `Promise` mais ce résultat à disposition de tout le code souscris lorsqu'il est prêt.

 voici la syntaxe du constructeur pour un objet `Promise` : 

 ```
 let promise = new Promise(function(resolve, reject) {
   // executor (the producing code)
 });
 ```

 La fonction après new Promise est appelée exécuteur. Quand une nouvelle promise est créee, l'exécuteur s'exécute automatiquement. Il contient le "code producteur" qui devrait éventuellement produire le résultat.

 Ses arguments `resolve` et `reject` sont des rappels fournis par javascript. Notre code est uniquement à l'interieur de l'exécuteur.

Lorsque l'exécuteur obtient le résultat, que ce soit tôt ou tard, peu importe, il doit appeler l'un de ces rappels:

*   `resolve(value)` si le travail est finit avec succès, avec comme résultat `value`

*   `reject(error)` si une erreur ce produit, `error` est l'objet d'erreur.

Donc pour résumer : l'exécuteur s'exécute automatiquement et tente d'effectuer un travail, une fois la tentative terminée, il appelle `resolve` si elle réussis
ou `reject` en cas d'erreur.

L'objet `promise` retourné par le constructeur `new promise` à ces propriétés interne : 

*   `state` initiallement `pending`, puis `fulfilled` quand `resolve` est appellé ou `reject` quand reject est appellé

*   `result` initiallement `undefined`, puis passe à `value` quand `resolve(value)` est appelé ou `error` quand `reject(error)` est appelé.

 