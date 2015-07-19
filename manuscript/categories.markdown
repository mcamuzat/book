# Les catégories

##Introduction
J'ai décidé de commencer à écrire sur le sujet des catégorie. 

Je ne suis pas vraiment à l'aise. Mon background n'a pas grand chose à voir.

Normalement c'est plutot pour les mathématiciens. Mais quand on regarde la programmation et surtout la programmation fonctionnelle.  On voit apparaitre le typage, les MapReduces, les promesses (promise), les multicore, monades. 

Tout cela vient un peu des catégories.

Est-ce que cela vaux le coup, je ne sais pas trop. Vous pouvez être un très bon programmeur et ne rien connaître des catégories. 

## Définition
Une categorie est composé d'**Objets** et de **Flèches**.

les **Objects** sont un peu près n'importe quoi. Cela n'a pas de rapport avec l'object de la programmation orienté objet.

les **fleches** sont la plupart du temps des fonctions qui vont d'un object à un autre d'objet. Je vais montrer des exemples
par exemple:

la fonction str_len() : prends en entrée une chaine de caractères `string` et en sortie un `integer`.
> `str_len : string -> integer`

la fonction str_upper() : prend en entrée une `string` renvoie une `string`

> `str_upper : string -> string`

de manière générale : `f : A -> B` 

pour la fonction à N arguments c'est plus incomfortables mais par exemple
la fonction `str_repeat (string, int)` devient
> `st_repeat : string -> integer -> string`

On peut bien entendu composer les fonctions
par exemple
> `f : A -> B`
> `g : B -> C`
> `g . f : A -> C`

en code source c'est plus simple ..
``` javascript
function gf(a){
	return g(f(a));
}
```
Il existe une fonction Identitée `Id` tels que `Id(a) = a`

Quand nous avons les objets, les flèches, l'identitée et la composition nous avons une **catégorie**

