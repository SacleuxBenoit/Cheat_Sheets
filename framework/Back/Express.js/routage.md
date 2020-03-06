## Routage

La définition de la route via la doc officiel: 
```
app.METHOD(PATH, HANDLER)
```

*   app c'est l'instance d'express 
```
const express = require('express')
const app = express()
```

*   METHOD peut comprendre : .GET .POST .PUT .DELETE etc, c'est une méthode de [demande http](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)

*   PATH c'est le chemin sur le serveur

*   et HANDLER c'est la fonction éxecuté lorsque la route est mise en correspondance.

