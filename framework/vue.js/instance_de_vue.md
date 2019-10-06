# Vue Js : 

## Instance de vue :

### créer un instance de vue : 

pour créer un instance de vue il faut faire : 
```
var vm = new Vue({
  // options
})
```
* Par convention, nous utilisons souvent la variable vm (abréviation pour ViewModel) pour faire référence au instances de Vue.

## Données et Méthodes : 

quand une instance de vue est créée, ça ajoute toutes les propriétés trouvés dans son objet data au système réactif de vue.
Quand une valeur de ces propriétés change, la vue va "réagir", se mettant à jour pour concorder avec les nouvelles valeurs.
```
// Notre objet de données
var data = { a: 1 }

// L'objet est ajouté à une instance de Vue
var vm = new Vue({
  data: data
})

// Récupérer la propriété depuis l'instance
// retourne celle des données originales
vm.a == data.a // => true

// assigner la propriété à une instance
// affecte également la donnée originale
vm.a = 2
data.a // => 2

// ... et vice-versa
data.a = 3
vm.a // => 3
```
quand ces données changent, le rendu de la vue est refait. il est à noter que les propriétés dans data sont réactives
si elles existaient quand l'instance a été créée.

si vous savez que vous allez avoir besoin d'une propriété plus tard qui n'a pas de valeur dès le début, vous avez juste besoin de la créer avec n'importe quelle valeur initiale, par exemple : 
```
data: {
  newTodoText: '',
  visitCount: 0,
  hideCompletedTodos: false,
  todos: [],
  error: null
}
```
la seule exception c'est l'utilisation de Ojbect.freeze(), qui empêche les propriétés existantes d'être changées,
le système de réactivité ne peut donc pas traquer les changements.

en plus des propriétés de données, les instances de vue exposent de nombreuses méthodes et propriétés. 
Les propriétés et méthodes sont préfixés par : $  pour les différencier des propriétés proxifiées de data.

