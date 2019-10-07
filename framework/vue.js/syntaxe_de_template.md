# Vue Js : 

## Syntaxe de template :

Vue js utilise une syntaxe de template basée sur le HTML, elle permet de lier déclarativement le DOM rendu au données de l'instance sous-jacente de vue. Tous les templates de vue sont du HTML valide qui peut être interprété par les navigateurs et les interpréteurs HTML.

## Interpolations : 

# texte : 

la forme la plus élémentaire de la liaison de données est l'interpolation de texte en utilisant la syntaxe "mustache" 

```
<span>Message: {{ msg }}</span>
```
La balise moustache sera remplacée par la valeur de la propriété msg de l'objet data correspondant.
Elle sera également mise à jour quand la propriété msg changera.

Nous pouvons également réaliser des interpolations à usage unique qui ne se mettront pas à jour lors de la 
modification des données en utilisant la directive v-once, mais il faut garder à l'esprit que cela affectera 
toutes les liaisons de données présentes sur le même noeud

```
<span v-once>Ceci ne changera jamais : {{ msg }} </span>
```

# Interprétation du HTML

Les doubles moustaches interprétent la données comme du texte brut et pas en tant qu'HTML. Pour afficher du HTML il faut 
utiliser la directive : v-html





