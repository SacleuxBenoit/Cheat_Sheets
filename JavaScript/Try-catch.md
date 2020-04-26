# Javascript

## try..catch

Lorsque nous avons un problème dans notre code celui-ci s'arrête immédiatement, nous pouvons faire un console.log pour voir ou est le problème, mais peut-on faire en sorte que si un problème est détecté dans une partie du code, au lieu de s'arrêter immédiatement, il exécute quelque chose d'autre ? la réponse est oui ! ... il suffit d'utiliser `try... catch` (il fonctionne de manière [synchrone](https://github.com/SacleuxBenoit/Cheat_Sheets/blob/master/JavaScript/SynchroneVsAsynchrone.md))

Voici la syntaxe :
```js
try{
    // Mettez votre code ici
}catch(err){
    // gestion de l'erreur ici
}
```

comme on peut le voir ci-dessus il y a 2 blocs : `try` et `catch`, premièrement la partie `try` est exécutée, s'il n'y a pas d'erreurs alors il ignore directement la partie `catch` et continue d'exécuter le reste du code, mais si une erreur est trouvée dans la partie `try` alors la partie `catch` est exécutée.

## Exemple de try...catch avec un code qui fonctionne
```js
try{
    console.log(Math.random(1,10))
}catch(err){
    console.log("Math.random is not working")
}
```

Ici `try` va être exécuté et comme il n'y a pas d'erreur dans le code, le code va correctement s'exécuter et ne pas passer dans la partie `catch`, un nombre aléatoire entre 1 et 10 va être affiché dans la console.

## Exemple de try...catch avec un code qui ne fonctionne pas

```js
try{
    console.log(Math.rand(1,10))
}catch(err){
    console.log("Math.random is not working")
}
```

Ici il y a un problème dans le 1er bloc, donc le `catch` va être exécuté et `"Math.random is not working"` va être affiché dans la console.

## Erreur 

Quand une erreur se produit, Javascript génère un objet contenant les détaille à propos de cette erreur. 

*   `name` : Nom de l'erreur, par exemple pour une variable non définie (ReferenceError)

*   `message` : Message textuel sur les détaille de l'erreur, il existe d'autres propriétés disponibles dans la plupart des environnements, l'un des plus utilisées et : `stack`

*   `stack`: une chaîne contenant des informations sur la séquence d'appels imbriqués qui ont conduit à l'erreur. Utilisé à des fins de débogage.

```js
try {
    rand; // error, variable is not defined!
  } catch(err) {
    console.log(err.name); // ReferenceError
    console.log(err.message); // rand is not defined
    console.log(err.stack); // ReferenceError: rand is not defined at (...call stack)
    // The error is converted to string as "name: message"
    console.log(err); // ReferenceError: rand is not defined
  }
```

Si nous n'avons pas besoin des détails de l'erreur, nous pouvons l'enlever :

```js
try{
    // Mettez votre code ici
}catch{
    // gestion de l'erreur ici
}
```
## Try...catch...finally

`Try...catch` peut venir avec `finally`, il s'exécute dans tous les cas, après `try` s'il n'y a pas d'erreur, ou après `catch` s'il y a une erreur.

Voici la syntaxe :

```js
try{
    // Mettez votre code ici
}catch{
    // gestion de l'erreur ici
}finally{
    // S'exécute toujours après Try si pas d'erreur, ou après catch s'il y a une erreur
}
```



