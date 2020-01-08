# Vue Js 

## Instance de vue 

### créer un instance de vue  

pour créer un instance de vue il faut faire : 
```
var vm = new Vue({
  // options
})
```
*   Par convention, nous utilisons souvent la variable vm (abréviation pour ViewModel) pour faire référence au instances de Vue.

## Données et Méthodes  

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
la seule exception c'est l'utilisation de Object.freeze(), qui empêche les propriétés existantes d'être changées,
le système de réactivité ne peut donc pas traquer les changements.

en plus des propriétés de données, les instances de vue exposent de nombreuses méthodes et propriétés. 
Les propriétés et méthodes sont préfixés par : $  pour les différencier des propriétés proxifiées de data.

## Hooks de cycle de vie d'une instance 

Chaque instance de vue traverse une série d'étape d'initialisation au moment de sa création, elle dois : 
mettre en place l'observation de données, compiler le template, monter l'instance sur le DOM et mettre à jours le DOM
quand les données changent. En cours de route elle va aussi invoquer des hooks de cycle de vie, qui nous donnent 
l'opportunité d'exécuter une logique personalisée à chaque niveau.

il y a des hooks qui sont appelés à différentes étapes du cycle de vie => created,mounted,updated,destroyed.
Tous ces hooks de cycle de vie sont appelés avec leur this pointant sur l'instance de la vue qui les invoque.

!!!!! Ne pas utiliser les fonctions fléchés sur une propriété ou fonction de rappel d'une instance.
Comme les fonctions fléchés sont liées au context parent, this ne sera pas l'instance de vue comme vous pourriez
vous y attendre, et vous rencontrerez alors des erreurs. !!!!!

![alt text](images/lifecycle.png)