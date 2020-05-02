# Javascript

## Caractères spéciaux

En Javascript il est possible d'ajouter des caractères spéciaux en utilisant le signe backslash `\`.

Le backslash est utilisé `échapper` le prochain caractère, par exemple pour la variable suivante

```js
let text = 'Il n'y a pas de fumée sans feu'
```

en output on va avoir : `SyntaxError: Unexpected identifier 'y'. Expected ';' after variable declaration.`

Pour régler ce problème il suffit de mettre un backslash avant les guillemets, Javascript va donc `Echapper` les guillemets :

```js
let text = 'Il n\'y a pas de fumée sans feu'
```

en output on va avoir : 'Il n'y a pas de fumée sans feu'.

## Liste des caractères spéciaux

Voici la liste de tous les caractères spéciaux que l'on peut utiliser avec le backslash.

*   `\'` peut échapper le single quote

Voila ce que ça va donner si on utilise pas l'antislash 

```js
let orcs = 'Je suis un orc Mag'har';
console.log(orcs) // SyntaxError: Unexpected identifier 'har'. Expected ';' after variable declaration.
```

et en utilisant l'antislash : 

```js
let orc = 'Je suis un orc Mag\'har'
console.log(orc) // Je suis un orc Mag'har
```

*   `\"` peut échapper le double quote

voici un exemple de ce que ça va donner si on utilise pas l'antislash : 

```js
let herboriste = "Je ramasse de la zin"anthide";
console.log(herboriste) // SyntaxError: Unexpected identifier 'anthide'. Expected ';' after variable declaration.
```

et ce que ça va donner en l'utilisant :

```js
let herbo = "Je ramasse de la zin\"anthide"
console.log(herbo) // Je ramasse de la zin"anthide
```

*   `\n` Nouvelle ligne 
*   `\r` carriage return
*   `\t` tab
*   `\b` backspace
*   `\f` form feed
