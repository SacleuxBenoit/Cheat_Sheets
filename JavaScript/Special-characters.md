# Javascript

## Caractères spéciaux

En Javascript il est possible d'ajouter des caractères spéciaux en utilisant le signe backslash `\`.

Le backslash est utilisé échapper le prochain caractère, par exemple pour la variable suivante

```js
let text = 'Il n'y a pas de fumée sans feu'
```

en output on va avoir : `SyntaxError: Unexpected identifier 'y'. Expected ';' after variable declaration.`

Pour régler ce problème il suffit de mettre un backslash avant les guillemets, Javascript va donc `Echapper` les guillemets :

```js
let text = 'Il n\'y a pas de fumée sans feu'
```

en output on va avoir : 'Il n'y a pas de fumée sans feu'.