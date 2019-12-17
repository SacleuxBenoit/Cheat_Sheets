# Markdown

## Dans ce cheat_sheet nous allons comparer comment écrire en Markdown par rapport au html

## Comment faire un paragraphe en Markdown ?

Pour faire un paragraphe en HTML il faut faire : 
```
<p>un paragraphe ici</p>

<p>un autre paragraphe ici</p>
```

Alors que pour faire un paragraphe en Markdown, il suffit de séparer le texte par des lignes vides :
```
un paragraphe ici

un autre paragraphe ici
```

## Emphase (italique / gras)

Pour faire de l'emphase (de la mise en valeur), il faut entourer le / les mots de notre choix par `*` ou `_`.
Il y a 2 types d'emphase : l'emphase faible, généralement affichée en italique et l'emphase forte, généralement affichée en gras.

### Emphase faible :

En html ce sera : 
```
<p>c'est un <em>mot</em> important</p>
```

alors qu'en Markdown :
```
c'est un *mot* important.

c'est un _mot_ important.
```

### Emphase forte :

en html ce sera : 
```
<p>c'est un <strong>mot</strong> important</p>
```

alors qu'en Markdown : 
 ```
c'est un **mot** important.

c'est un __mot__ important.
 ```

 ## Les Titres

 pour écrire un titre en html on fait : 
 ```
<h1>C'est un titre de niveau1</h1>
<h2>C'est un titre de niveau2</h2>
<h3>C'est un titre de niveau3</h3>
 ```

Alors qu'en Markdown il suffit de faire :
```
# C'est un titre de niveau1
## C'est un titre de niveau2
### C'est un titre de niveau3
```

il existe même une autre syntaxe pour les titres de niveau 4 et plus

## Les listes à puces

Pour faire une liste à puce en HTML il faut faire :
```
<ul>
<li>Une puce</li>
<li>Une autre puce</li>
<li>Et la dernière puce</li>
</ul>
```
et en markdown il faut faire :
```
* Une puce
* Une autre puce
* et la dernière puce
```