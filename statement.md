# Python, où commencer ?

Vous voulez apprendre à coder en Python ? 
Pour ça, il faut pouvoir écrire du code et pouvoir le lire.

Ecrire du Python est très simple. Sur Windows, Bloc-notes suffit, bien que ça ne soit pas pratique du tout (nous verrons pourquoi plus tard).
Par contre, pour exécuter le code Python que l'on peut écrire, c'est moins simple. Il faut doter l'orginateur d'un moyen de le comprendre 
et d'exécuter les instructions qui s'y trouve. Pour ça, il faut ce qu'on appelle un **interpréteur** Python.

Le site sur lequel vous consultez ce cours permet déjà de faire les deux, 
**écrire** et **exécuter** le code Python, dans une fenètre de code exécutable.

Dans la fenètre sous ce paragraphe se trouve écrit du texte respectant la syntaxe Python. Vous pouvez exécuter ce code en appuyant
 sur le bouton "RUN" :

```python runnable
print('Hello World!')
```

## Qu'est ce que le code ?

Le code se décompose en trois concepts :

1. La **syntaxe**, l’ensemble des règles formelles qui définissent comment écrire du code Python. La syntaxe détermine si le code est correctement formé.
2. Le **lexique**, le vocabulaire du langage. Le lexique détermine quels éléments peuvent être utilisés dans une instruction.
3. La **sémantique**, le sens du code, ce qu’il fait réellement. Deux lignes de code peuvent avoir une syntaxe correcte et utiliser le bon lexique, 
    mais produire des effets très différents. La sémantique couvre la logique des programmes, les comportements des fonctions, 
    la manière dont les objets interagissent, et les conséquences de chaque instruction.

Pour le code `print('Hello World!')`, voici en détails chacune des trois caractéristiques vue précédemment :

1. **Syntaxe** : Ce code est une expression (*Expr*). Cette expression est un appel (*Call*), 
    composé d'un nom et d'arguments entre parenthèses. Il y a un argument, une constante, dont 
    la valeur est `'hello world!'`.
2. **Lexique** : Il est composé de 4 mots, ou briques lexicales : `print`, `(` et `)`, et `'Hello World!'`.
3. **Sémantique** : Et ce qu'il signifie dans ce cas est simple : afficher le texte `Hello World!` dans 
    la [sortie standard](https://fr.wikipedia.org/wiki/Flux_standard#Sortie_standard), ici la fenêtre de résultat de votre navigateur.

Changez un élément de la syntaxe, en retirant par exemple une parenthèse 
(toute parenthèse ouverte doit être fermée, et toute parenthèse fermante doit avoir été ouverte préalablement !), 
et la syntaxe n'est plus correcte, ce qui fait planter le programme :

```python runnable
print('Hello World!'
```

Changez le lexique en remplaçant par exemple les parenthèses par des crochets, des "mots" connus de Python, et il *peut* ne pas
y avoir de plantage (notez l'ajout d'un contexte particulier, nécessaire pour montrer que ce lexique, bien que différent, est correcte) :

```python runnable
print = {'Hello World!': None}  # contexte

print['Hello World!']
```

Sauf que dans ce cas là, rien ne se passe. Pas de plantage, mais pas de texte affiché. Simplement parce que la sémantique du code, 
"ce qu'il veut dire", est différent. En changeant le lexique utilisé, nous avons changé le sens du code. 
La ligne ajouté au dessus ne sert qu'à rendre ce code "logique", mais si vous retirez la ligne 
(essayez donc en modifiant directement le code et en appuyant sur "RUN" !), le lexique est le même, mais il n'a plus un sens logique.
Dans ce cas, Python va planter, affichant une erreur car vos instructions n'ont pas de sens.