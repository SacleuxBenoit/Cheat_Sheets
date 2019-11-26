# TypeScript

## Introduction

## Les variables dans TypeScript

Le principal atout de TypeScript c'est d'associer facultativement un type à une données.
```
let pi: number;
let message: string;
var flag: boolean;
var joker: any;
```

Dans l'exemple ci-dessus quatre variables sont déclarées sans être initialisées.

* La variable pi a pour type : number c'est un nombre entier ou flottant

* La variable message a pour type : string c'est une chaine de caractères

* La variable flag a pour type : boolean il peut prendre true or false

* La variable joker a pour type any : c'est le type par défaut que TypeScript attribue pour une variable globale si il ne parviens pas à
déterminer son type lors de la déclaration