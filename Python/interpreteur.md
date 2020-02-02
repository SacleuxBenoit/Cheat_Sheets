# Python

## à quoi ça sert

L'interpréteur de commande permet de tester du code au fur et à mesure.

## Comment l'ouvrir

Pour aller sur l'interpréteur de python il faut faire la commande suivante dans votre terminal
```bash
python
```
un message comme celui ci-dessous devrait apparaître :
```bash
Python 2.7.16 (default, Oct 16 2019, 00:34:56) 
[GCC 4.2.1 Compatible Apple LLVM 10.0.1 (clang-1001.0.37.14)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

## Les premiers calculs

### Saisir un nombre 

Vous pouvez saisir un nombre après les `>>>` par exemple si on écrit 2, voila ce que ça donne
```bash
>>> 2
2
```

on saisit un nombre et l'interpréteur le renvoie, on peut aussi mettre des nombres à virgules, comme des nombres négatifs.

## Addition, soustraction, multiplication et division

Pour effectuer les opérations il faut utiliser les opérations suivantes `+` `-` `*` et `/`, par exemple :
```bash
>>> 2 + 2
4
```

## Division entière et modulo 

le résultat d'une division est données avec un nombre flottant :

```bash
>>> 10 / 5
2.0
>>> 10 / 3
3.3333333333333335
```

il existe 2 autres opérateurs qui permettent de connaître le résultat d'une division entière et le reste de la division : 
```bash
>>> 10 / 5
2.0
>>> 10 / 3
3.3333333333333335
```

Le premier opérateur utilise le symbole `//`, ça permet d'obtenir la partie entière d'une division.
```bash
>>> 10 / 3
 3
```

le deuxième opérateur `%` (modulo), permet d'obtenir le reste de la division
```bash
>>> 10 / 3
1
```