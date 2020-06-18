## Javascript

## Boucle While

### Description

La boucle `while` va nous permettre d'exécuter un ensemble d'instructions de façon répétés

### Syntaxe

Voici la syntaxe :

```js
while(condition){
    // code here
}
```

pendant que la condition est `true` le code est exécuté jusqu'à ce que la condition soit `false`

```js
let i = 10

while(i > 0){
    alert(i--)
} // Fait un décompte et affiche 10,9,8,7,6,5,4,3,2,1
```

Pour l'exemple ci-dessus, on dit que : `pendant que` i est plus grand que 0 alors tu rentres dans le body et tu exécutes `alert(i--)`, à chaque fois que l'on rentre dans le body on dit que l'on fait une itération, pour cet exemple il y a donc 10 itérations

il faut aussi savoir que les accolades ne sont pas obligatoires quand il n'y a qu'une seule instruction dans le body

par exemple :

```js
while(i > 0) alert(i--) // Fait aussi un décompte et affiche 10,9,8,7,6,5,4,3,2,1
```
