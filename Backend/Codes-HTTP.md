# Backend

## Description

Un code HTTP que l'on appel aussi `status code`, permet de définir le résultat d'une requête, il est divisé en 5 parties :

*   [100-199](#199) : C'est la partie `Information`, c'est une réponse provisoire
*   [200-299](#299) : Ici c'est le `succès` de la requête 
*   300-399 : C'est le code qui est lié à la `redirection`
*   400-499 : `Erreur dans la requête`
*   500-599 : `Erreur au niveau du serveur`

### Partie Information 100-199 <a id="199"></a>

| Code | Message | Description |
| ----------- | ----------- | ----------- |
| 100 | Continue | Le serveur renvoie ce code pour indiquer qu'il a reçu la première partie de la demande et attend le reste |
| 101 | Switching protocols | Changement de protocole accepté par le serveur, le protocole ne devra être changé que si il est avantageux de le faire |
| 102 | Processing | Traitement en cours, (évite que le client dépasse le temps d'attente limite, se ferme et provoque l'erreur 499) |

### Partie succès 200-299 <a id="299"></a>

| Code | Message | Description |
| ----------- | ----------- | ----------- |
| 200 | OK | Indique la réussite de la requête, la signification de la réussite dépend de la méthode de requête utilisée |
| 201 | Created | Indique que la requête a était traité avec succès et qu'une ressource a était créée |
| 202 | Accepted | Indique que la requête a été reçus, mais qu'aucune action n'a été entreprise|
| 203 | Non-Authoritative Information | L'information retournée n'a pas été générée par le serveur HTTP, mais par un autre source non authentifiée |
| 204 | No content | Le serveur HTTP a correctement traité la requête, mais il n'y a pas d'information à envoyer en retour |
| 205 | Reset content | La page courante peut être effacée, il indique au client qu'il doit remettre à zéro le formulaire utilisé |
| 206 | Partial content | Le serveur retourne une partie de la taille demandée, ce code est utilisé lorsqu'une requête spécifiant la taille à été transmise |
| 207 | Multi status | Ce code est principalement utilisé par le serveur WebDAV, il indique au client que plusieurs opérations se sont produites et que l'état de chaque opération peut être trouvé dans le corps de la réponse |
| 208 | Already reported | Ce code est principalement utilisé par le serveur WebDAV, élément de réponse propstat pour éviter d'énumérer les membres internes de plusieurs liaisons à la même collection à plusieurs reprises |
| 210 | Content different | Ce code est principalement utilisé par le serveur WebDAV, La copie de la ressource côté client diffère de celle du serveur (contenu ou propriétés) |
| 226 | IM used | Le serveur a accompli la requête pour la ressource, et la réponse est une représentation du résultat d'une ou plusieurs manipulations d'instances appliquées à l'instance actuelle |