# JavaScript

## Map

`Map` est une collection de données à clé,tout comme un objet. Mais la principale différence c'est que `Map`autorise les clés de tout type.

les Methods et les properties sont : 

*   new Map() - crée la map.
*   map.set(key, value) - stocke la valeur par la clé.
*   map.get(key) - renvoie la valeur par la clé, non définie si la clé n'existe pas dans `Map`
*   map.has(key) - retourne `true`si la clé existe, sinon retourne `false``
*   map.delete(key) - supprime la valeur de la clé.
*   map.clear() - supprime tout de `Map`
*   map.size() - renvoie le nombre d'éléments actuel

Par exemple : 
```javascript
let map = new Map();

map.set('1', 'str1'); // a string key
map.set(1, 'num1'); // a numeric key
map.set(true, 'bool1'); // a boolean key


alert(map.get(1) ); // 'num1'
alert(map.get('1') ); // 'str1'
alert(map.size); // 3
```
Comme nous pouvons le voir, contrairement aux objets, les clés ne sont pas convertis en string. Tout type de clé est possible

Map peut aussi utiliser des objets comme clés.

par exemple : 
```javascript
let john = { name : "john"};

let visitsCountMap = new Map();

visitsCountMap.set(john,123);

alert(visitsCountMap.get(john) ); // 123 
```

l'utilisation d'objets comme clés est l'une des fonctionnalités Map les plus importantes.