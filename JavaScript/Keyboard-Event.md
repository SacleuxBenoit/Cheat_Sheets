# Javascript 

## Description

En Javascript il existe 3 types d'événement pour l'utilisation d'une touche au clavier 

*   `keydown` C'est lorsque l'on enclenche une touche. 
*   `keypress` C'est lorsque l'on enclenche une touche `produisant un caractère`, sauf que c'est devenu obsolète et il n'est pas compatible avec tous les navigateurs.
*   `keyup` C'est lorsque l'on relève une touche.

## event.key et event.code

*   Pour la propriété `key` on va directement renseigner le caractère

```js
message.addEventListener('keydown', (e) => {
    if(e.key == "z"){
        console.log("Z à était press")
    }
})
```

*   Tandis que pour la propriété `code` il va falloir obtenir un code spécial, pour trouver quel code correspond à la touche que l'on souhaite entrer, on peut utiliser le site [keycode.info](https://keycode.info) il suffit d'appuyer sur une touche et le site va directement vous donner le code pour cette touche

```js
message.addEventListener('keydown', (e) => {
    if(e.keyCode == "65"){
        console.log("A à était press")
    }
})
```