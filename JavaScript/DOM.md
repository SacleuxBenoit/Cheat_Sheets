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

Si nous utilisons `document.body` dans la balise `head`, nous allons avoir un problème, `null` va être affiché, car dans le DOM la valeur `nul` veut dire `n'existe pas`

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