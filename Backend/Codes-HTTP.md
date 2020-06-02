# Backend

## Description

Un code HTTP que l'on appel aussi `status code`, permet de définir le résultat d'une requête, il est divisé en 5 parties :

*   100-199 : C'est la partie `Information`, c'est une réponse provisoire
*   200-299 : Ici c'est le `succès` de la requête 
*   300-399 : C'est le code qui est lié à la `redirection`
*   400-499 : `Erreur dans la requête`
*   500-599 : `Erreur au niveau du serveur`

### Partie Information 100-199

```markdown
| Code | Message | Description |
| ----------- | ----------- | ----------- |
| 100 | Continue | Le serveur renvoie ce code pour indiquer qu'il a reçu la première partie de la demande et attend le reste |
| ----------- | ----------- | ----------- |
| 101 | Switching protocols | Changement de protocole accepté par le serveur, le protocole ne devra être changé que si il est avantageux de le faire |
| ----------- | ----------- | ----------- |
| 102 | Processing | Traitement en cours, (évite que le client dépasse le temps d'attente limite, se ferme et provoque l'erreur 499) |
```