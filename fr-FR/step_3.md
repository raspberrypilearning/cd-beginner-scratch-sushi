## Ajouter et supprimer des blocs de code

Génial! Tu as écrit ton tout premier programme Scratch. Il est temps d'en apprendre un peu plus sur l'introduction et la suppression de code dans Scratch! Le code Scratch est composé de **blocs** tels que:

![](images/code1.png)

Tu trouveras tous les blocs dans la **palette des blocs de code**, classés en différentes catégories en fonction de ce qu'ils font.

## \--- collapse \---

## title: Utiliser des blocs de différentes catégories

Clique sur un nom de catégorie pour voir les blocs de cette catégorie. Ici, la catégorie **Mouvement** est sélectionnée:

![](images/code2a.png)

Tous les blocs de la catégorie sur laquelle tu as cliqué sont affichés dans une liste:

![](images/code2b.png)

Tu peux cliquer sur le bloc que tu cherches, puis le faire glisser dans le panneau du sprite actuel, puis lâcher le bouton de la souris. Une fois que le bloc est dans le panneau, tu peux le déplacer et le relier à d'autres blocs.

\--- /collapse \---

Si tu veux voir ce que fait un bloc, tu peux double-cliquer dessus pour le faire exécuter!

\--- task \--- Essaie de double-cliquer sur certains blocs pour voir ce qu’ils font. \--- /task \---

## \--- collapse \---

## title: Exécuter le code

Généralement, tu veux que ton code soit exécuté automatiquement chaque fois que quelque chose de spécifique se produit. C’est pourquoi beaucoup de tes programmes commenceront avec un bloc de la catégorie **Événements** , le plus souvent celui-ci:

```blocks3
    quand le drapeau vert est cliqué
```

Les blocs de code reliés à ce bloc seront exécutés après que le **drapeau vert** sera cliqué.

Les blocs de code s'éxécutent du haut en bas. L'ordre dans lequel tu assembles tes blocs est donc important. Dans cet exemple, le sprite `dira`{:class = "block3looks"} `Bonjour!` avant de `jouer`{:class = "block3sound"} le son `Meow`.

```blocks3
    quand le drapeau vert est cliqué
    dire [Bonjour]
    jouer le son [Meow v]
```

\--- /collapse \---

Il est facile d'enlever ou de supprimer des blocs de code que tu ne veux pas dans ton programme! Fais-les simplement glisser dans la palette des blocs de code.

**Fais attention:** si tu fais glisser un bloc de code dans la palette des blocs de code, ce supprimera tous les blocs reliés au bloc que tu fais glisser. Veille donc à séparer les blocs de code que tu souhaites conserver de ceux que tu souhaites enlever. If you delete some code blocks by accident and want to get them back, right-click and then click on the **undo** option to get everything back.

![](images/code6.png)

\--- task \--- Try adding, deleting, and undeleting some code blocks! \--- /task \---

### Putting it all together

Now you know how to move code around and make things happen, it's time for you to create a program to make the Scratch Cat walk in a circle!

\--- task \--- Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. You’ll find them in the **Events** and **Motion** lists.

```blocks3
    when green flag clicked
    move [10] steps
```

\--- /task \---

\--- task \--- Now, click on the green flag above the Stage.

![](images/code7.png) \--- /task \---

You should see the cat walking in a straight line...not exactly what you want, right?

Note: If you click th flag too many times and the cat walks away, you can drag it back!

\--- task \--- Snap the turn block to the end to make the cat sprite walk in a circle. It’s in the **Motion** list too.

```blocks3
    when green flag clicked
    move [10] steps
+    turn cw (15) degrees
```

\--- /task \---

## \--- collapse \---

## title: How does turning work?

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. You can change that number, and the number of steps, by clicking on the number and typing in a new value.

![](images/code9.png)

\--- /collapse \---

\--- task \--- Now save your work! \--- /task \---