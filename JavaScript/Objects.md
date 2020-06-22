# Object

Un objet peut être créé en utilisant les brackets `{ }`, avec une liste (facultative) de propriété. Une propriété c'est : `clé : valeur` 

Il existe 2 façons de créer un objet
```js
let client = new Object();
let client = {}
```

Maintenant que nous avons vu comment créer un objet, nous allons voir ce qu'est la `clé` et la `valeur`

```js
let firstClient = {
    name : "Gérard", // clé = name, valeur = "Gérard"
    age : 45, // clé = age, valeur = 45
    eyes : 2 // clé = eyes, valeur = 2
};
```

comme nous pouvons le voir avec l'exemple au-dessus, la `clé` est à gauche avant `:` et sur la droite nous avons la `valeur`.

### Accéder / Modifier la valeur

nous pouvons lire, ajouter ou encore enlever une valeur.

Pour lire une valeur il faut utiliser le nom de l'objet suivit d'un point `.` et ensuite mettre la `clé` :

```js
console.log(firstClient.name) // "Gérard"
console.log(firstClient.age) // 45
console.log(firstClient.eyes) // 2
```

Si nous voulons enlever une valeur il va falloir mettre `delete` suivis de `nom de l'objet.clé`

```js
delete firstClient.age // {name : "Gérard", eyes : 2}
```

et enfin, si nous voulons ajouter une valeur il faudra faire : 

```js
firstClient.newvalue = true // {name : "Gérard", eyes : 2, newvalue : true}
```

Si jamais nous voulons utiliser une clé avec 2 mots ou + il va falloir utiliser les guillemets :

```js
let Orc = {
    arms : 2,
    legs : 2,
    skill : "unknown",
    "class and spec" : "unknown"
}
```

Par contre, lorsque nous voudrons changer sa valeur, nous allons devoir faire comme ci-dessous : 

Lire une valeur :

```js
console.log(Orc["class and spec"]) // unknown
```

Supprimer une valeur :

```js
delete Orc["class and spec"] // {arms: 2, legs: 2, skill : "unknownn"}
```

Ajouter une valeur :

```js
Orc["class and spec"] = "Hunter BM" // {arms: 2, legs: 2, skill : "unknownn", class and spec : "Hunter BM"}
```