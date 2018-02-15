# Commandes
## Sheebang
Le sheebang permet de définir quel sera l'interpréteur qui sera utilisé pour exécuter le script si on execute le fichier.

Il doit être définit à la première ligne du script.
~~~bash
#!/bin/sh
~~~

Exemple :
~~~bash
./monscript
~~~
La commande suivante utilisera l'interpréteur définit par le sheebang.

## Arguments
### Nom du script
~~~bash
$0
~~~
Peut être pratique dans le cas où le script est déplacé puis renommé.

### Arguments du script
~~~bash
$1... $n
~~~

Tous les arguments en une seule variable
~~~bash
$@
~~~

### Code retour
~~~bash
$?
~~~
Code retour de la précédente commande

### Nombre d'arguments
~~~bash
$#
~~~
Nombre d'arguments à l'appel du script

## Variables

### Déclaration

~~~bash
mavariable=0
~~~
On peut créer une variable à n'importe quel endroit dans le script.
> Note : Il faut absolument ne pas laisser d'espaces entre le nom de la variable et sa valeur d'affectation

### Utilisation
Pour exploiter la valeur d'une variable, il faut utiliser l'opérateur **$**.

Exemple :
~~~bash
mavariable=3
echo "Contenu de la variable : $mavariable"
~~~

Ce qui affichera :
~~~bash
Contenu de la variable : 3
~~~

## Quotes

### Double quotes
Elles permettent d'afficher du texte et interprètent les variables présentes dans la chaîne.
Exemple :
~~~bash
mavariable=3
echo "Contenu de la variable : $mavariable"
~~~

Ce qui affichera :
~~~bash
Contenu de la variable : 3
~~~

### Quotes simples
 Les quotes simples permettent de n'afficher que du texte, et empêchent l'interprétation de variables dans la chaîne.
 
 Exemple :
~~~bash
mavariable=3
echo 'Contenu de la variable : $mavariable'
~~~

Ce qui affichera :
~~~bash
Contenu de la variable : $mavariable
~~~

### Les anti-quotes
Les anti-quotes permettent d'exécuter une commande dans une autre commande
Exemple :
~~~bash
echo "Le fichier fait `cat monfichier | wc -l` lignes"
~~~

On peut également utiliser l'opérateur **$(commande)** :
~~~bash
echo "Le fichier fait $(cat monfichier | wc -l) lignes"
~~~

## Sources
[https://www.shellscript.sh/index.html](https://www.shellscript.sh/index.html) 

## TODO 
- Fonctions
	- Créer une fonction
	- Appeler une fonction
	- Fonctions retournant une valeur
		- _return_
		- Récupération de la valeur
- Portées
	- global
	- local

