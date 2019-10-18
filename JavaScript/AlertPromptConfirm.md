# JavaScript

## Interaction : Alert, Prompt, Confirm.

### Alert : 

La syntaxe de `Alert` :
```
alert(message);
```

ça affiche un message et met en pause l'exécution du script jusqu'à ce que l'utilisateur appuie sur le bouton "ok"

la mini-fenêtre qui s'ouvre s'appelle une fenêtre modale, le "modale" signigie que le visiteur ne peut pas interagir avec le reste de la ppage
tant qu'il n'a pas appuyer sur le bouton "ok".

### Prompt :

la syntaxe de `Prompt` : 
```
result = prompt(title [default]);
```

la fonction prompt accepte 2 arguments, elle affiche une fenêtre modale avec 2 bouton ok et annuler 

`title` c'est le text à afficher au visiteur.

`defaut` c'est un autre paramètre mais qui est facultatif c'est pour donner la valeur initial du champ

le prompt renvoie `Null` si ont appuye sur la touche `echap`.

### Confirm : 

La syntaxe de confirm :
```
result = prompt(question)
```

Confirm affiche une fenêtre modale avec 2 boutons : `ok` et `annuler`.

c'est true si `ok` est appuyé et false si `annuler` est appuyé.







