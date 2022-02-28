# Doc python

### Affichage

Pour afficher quelque chose : `print` par exemple 
```python
print("Hello World")
```
va afficher le message Hello World.

### Commentaires

*   Pour mettre une ligne en commentaire, il faut utiliser `#`
*   pour du multi ligne, il suffit d'utiliser le `#` au début de chaque ligne

### Variables

Pour les noms de variables, il faut respecter quelques conventions :
*   Le nom doit commencer par une lettre ou un underscore
*   le nom de la variable ne doit pas contenir d'espace

Les noms de variables sont sensible à la casse, par exemple `MyVar` et `myvar` sont 2 variables différents
pour créer une variables : `MyVar = 2` le signe `=` sert d'assignation.

Pour changer le contenu d'une variable : `MyVar = "deux"`.
Si ont fait `print(MyVar)` "deux" va donc être affiché au lieu de "2"


## Les types

### type numérique

*   `int` représente tout entier positif comme négatif
*   `float` représente les nombres décimaux et certaines expressions scientifiques comme le `e` pour exponentielle
*   `complex` représente les nombres complexes ou imaginaires (lettre `j` pour la partie imaginaire d'un nombre).

### chaine de caractères

pour une chaine de caractères, il faut utiliser les guillemets au début et à la fin : `greetings = "Hey, how are you ?"`.
Si l'ont veut concaténer deux chaines de caractères il suffit d'utiliser le `+` entre les 2 chaines.

### type booléan 

il existe 2 réponses possible pour un type booléan :

*   `True`
*   `False`
```python
b = true
print(b)
# true
```