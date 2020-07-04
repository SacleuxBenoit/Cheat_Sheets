# Javascript

## qu'est-ce que le DOM

Le DOM `Document Object Model` c'est une interface pour nos pages web, c'est en quelque sorte une représentation du HTML, il permet d'accéder aux éléments d'une page web afin de modifier le contenu avec un autre language, comme par exemple le javascript

## Accéder au DOM

Le DOM nous permet de modifier les éléments comme nous le voulons, pour pouvoir y accéder on va utiliser l'objet `document` par exemple pour modifier le background-color :

```js
document.body.style.background = "blue";
```

*   Pour pouvoir accéder à la balise `<html>` `document.documentElement` (c'est le noeud le plus haut)
*   Si nous voulons accéder au body `document.body`
*   Et pour le tag `head` `document.head`
*   Etc...

## null

Si nous utilisons `document.body` dans la balise `head`, nous allons avoir un problème, `null` va être affiché, car dans le DOM la valeur `null` veut dire `n'existe pas`

```html
<html>

<head>
  <script>
    alert( "à partir de HEAD: " + document.body ); // affiche null, il n'y a pas de <body>
  </script>
</head>

<body>

  <script>
    alert( "à partir du BODY: " + document.body );
  </script>

</body>
</html>
```

## getElementById

Si par exemple nous voulons appliquer une couleur spécifique sur un paragraphe lorsque l'on clique sur un bouton, on va utiliser `getElementById` pour récupérer l'id du paragraphe en question et lui ajouter une couleur 

```js
function changeColor(newColor){
    let change = document.getElementById("parColored"); // on récupère l'id "parColored" et on la met dans la variable change
    change.style.color = newColor
}
```

et dans le html on va avoir :

```html
<div id="parColored">
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam, ullam inventore commodi consectetur nulla totam quisquam recusandae voluptatem maxime veniam quae dolorem expedita dolorum accusamus nostrum vero voluptatum labore blanditiis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. Excepturi itaque eveniet est molestiae magnam vero quaerat mollitia assumenda necessitatibus velit ab quidem vel, et accusamus beatae? Id qui laudantium fugiat! Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam obcaecati, magni id similique, alias quis animi vero corrupti optio earum quia doloribus voluptatibus enim, veniam beatae odit reiciendis laudantium unde.
    </p>
    <button onclick="changeColor('blue')">Texte en bleu</button>
```

lorsque nous cliquons sur le bouton, le paragraphe va donc se changer en bleu