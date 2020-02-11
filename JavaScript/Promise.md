# Javascript

## Promise

*   Un "code producteur" qui fait quelque chose et qui prend du temps. par exemple : du code qui charge les données sur un réseau.

*   un "code consommateur" qui veut le résultat du "code producteur" une fois prêt. Beaucoup de fonctions peuvent avoir besoin de ce résultat.

*   Une `Promise` est un objet Javascript spécial qui relie le "code producteur" et le "code consommateur". Le "code producteur" prend le temps dont il a besoin pour produire le résultat promis, et la `Promise` mais ce résultat à disposition de tout le code souscris lorsqu'il est prêt.

voici la syntaxe du constructeur pour un objet `Promise` : 

```
let promise = new Promise(function(resolve, reject) {
  // executor (the producing code)
});
```