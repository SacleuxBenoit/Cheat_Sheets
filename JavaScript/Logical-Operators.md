# Javasript

## Opérateur logique

En javascript il existe 3 types d'opérateur logique : OR `||`, AND `&&`, NOT `!`, ils peuvent être appliqués à tous types de valeurs.

### L'opérateur OR ||

Voici la syntaxe : 

```js
result = true || false
```

Il faut savoir que :

*   l'opérateur `OR` évalue l'opérande de la gauche vers la droite
*   il converti chaque opérande en booléen
*   si le résultat est `true ` alors il s'arrête et retourne la valeur
*   si tous les opérandes sont `false` alors il retourne le dernier opérande