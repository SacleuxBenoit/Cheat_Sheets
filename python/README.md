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

Pour une chaine de caractères, il faut utiliser les guillemets au début et à la fin : `greetings = "Hey, how are you ?"`.

*   `concaténation` Si l'ont veut concaténer deux chaines de caractères il suffit d'utiliser le `+` entre les 2 chaines.

*   `opérateur de répétition` l'opérateur de répétition c'est : `*` ça va nous permettre de répéter une chaine un certain nombre de fois.
    exemple : `username=toto` si l'on fait `4 * toto` ça équivau à `totototototototo`.

### type booléan 

il existe 2 réponses possible pour un type booléan :

*   `True`
*   `False`

```python
b = true
print(b)
# true
```

### Connaître le type d'une valeur

pour ce faire, il va falloir utiliser la fonction `type()`.
```python
str = "a string"
num = 2

print(type(str))
print(type(num))
# Pour str : affiche <classe 'str'>
# Pour num : affiche <classe 'int'> 
```

### Les listes

les listes ressemblent au `array` de JS : 

```python
firstList = [2,4,6,8,10]
print(firstList)
# Affiche [2,4,6,8,10]
```

encore un exemple :
```python
prenom = ["pierre","paul","jacque"]
print(prenom)
# Affiche ["pierre","paul","jacque"]
```

pour récupérer une valeur en particulier dans la liste il va falloir spécifier le nom de la liste suivit de la valeur entre crochet
l'indice -1 correspond au dernier element du tableau, le -2 à l'avant dernier etc.

```python
print(prenom[0])
# Affiche "pierre"
print(prenom[-1])
# Affiche "jacque"
```