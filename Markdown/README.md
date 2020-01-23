# Markdown

## Dans ce cheat_sheet nous allons comparer comment écrire en Markdown par rapport au html

### note 

même si ce cheat_sheet est une comparaison entre le HTML et le Markdown, il faut savoir que le Markdown est exporté en html 
vous pouvez donc utiliser du HTML dans vos pages Markdown.
Les fichiers Markdown sont enregistrés avec l'extension `.md` ou `.markdown`

## Comment faire un paragraphe en Markdown 

Pour faire un paragraphe en HTML il faut faire : 
```html
<p>un paragraphe ici</p>

<p>un autre paragraphe ici</p>
```

Alors que pour faire un paragraphe en Markdown, il suffit de séparer le texte par des lignes vides :
```markdown
un paragraphe ici

un autre paragraphe ici
```

## Emphase (italique / gras)

Pour faire de l'emphase (de la mise en valeur), il faut entourer le / les mots de notre choix par `*` ou `_`.
Il y a 2 types d'emphase : l'emphase faible, généralement affichée en italique et l'emphase forte, généralement affichée en gras.

### Emphase faible 

En html ce sera : 
```html
<p>c'est un <em>mot</em> important</p>
```

alors qu'en Markdown :
```markdown
c'est un *mot* important.

c'est un _mot_ important.
```

### Emphase forte 

en html ce sera : 
```html
<p>c'est un <strong>mot</strong> important</p>
```

alors qu'en Markdown : 
 ```markdown
c'est un **mot** important.

c'est un __mot__ important.
 ```

 ## Les Titres

 pour écrire un titre en html on fait : 
 ```html
<h1>C'est un titre de niveau1</h1>
<h2>C'est un titre de niveau2</h2>
<h3>C'est un titre de niveau3</h3>
 ```

Alors qu'en Markdown il suffit de faire :
```markdown
# C'est un titre de niveau1
## C'est un titre de niveau2
### C'est un titre de niveau3
```

il existe même une autre syntaxe pour les titres de niveau 4 et plus

## Les listes à puces

Pour faire une liste à puce en HTML il faut faire :
```html
<ul>
<li>Une puce</li>
<li>Une autre puce</li>
<li>Et la dernière puce</li>
</ul>
```
et en markdown il faut faire :
```markdown
* Une puce
* Une autre puce
* et la dernière puce
```

## Les listes à puces numérotées 

Pour faire une liste à puces numérotées en html il faut faire :
```html
<ol>
<li>Une puce</li>
<li>Une autre puce</li>
<li>Et la dernière puce</li>
</ol>
```

Alors que pour le Markdown c'est assez intuitif, il suffit mettre des numéros devant les puces !
```markdown
1. Une puce
2. Une autre puce
3. Et la dernière puce
```

## Code non exécuté

Pour ne pas exécuter du code en html on doit faire : 
```html
<code><h1>un titre ici</h1></code>
```

Alors que pour afficher du code en markdown il faut faire : 
```markdown
``` # un titre ici```
```
## Les liens

Pour faire un lien en html il faut faire : 
```html
<a href="https://github.com/SacleuxBenoit">Mon Github</a>
```

Alors que pour le Markdown, ont doit mettre le texte du lien entre crochets suivis du lien entre parenthèses :
```markdown
[Mon Github](https://github.com/SacleuxBenoit)
```

## Les images

Pour l'html : 
```html
<img src="mon_image.png" alt="mon image"/>
```

Pour le markdown c'est la même chose que les liens sauf que l'on rajoute un `!` devant les crochets : 
```markdown
![mon image](mon_image.png)
```

## Les tableaux

Pour faire un tableau en html il faut faire :
```html
<table>
   <tr>
       <td>Maison</td>
       <td>4 pièces</td>
       <td>États-Unis</td>
   </tr>
   <tr>
       <td>Studio</td>
       <td>2 pièces</td>
       <td>France</td>
   </tr>
</table>
```

et en Markdown :
```markdown
| Maison | 4 pièces | États-Unis |
| ----------- | ----------- | ----------- |
| Studio | 2 pièces | France |
```