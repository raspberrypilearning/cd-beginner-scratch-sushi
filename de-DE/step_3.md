## Adding and removing code blocks

Great! Du hast dein allererstes Scratch-Programm geschrieben. Zeit, etwas mehr darüber zu lernen, wie Code in Scratch ein- und ausgeblendet wird! Der Scratch-Code besteht aus **Blöcken** wie diesen:

![](images/code1.png)

You will find all blocks in the **code blocks palette**, sorted into different categories according to what they do.

## \--- collapse \---

## title: Verwenden von Blöcken aus den verschiedenen Kategorien

Klicke auf einen Kategorienamen, um die Blöcke in dieser Kategorie anzuzeigen. Hier wird die Kategorie **Bewegung** ausgewählt:

![](images/code2a.png)

Alle Blöcke in der Kategorie, auf die du geklickt hast, werden in einer Liste angezeigt:

![](images/code2b.png)

Du kannst auf den gewünschten Block klicken, ihn dann in das aktuelle Figuren-Panel ziehen und loslassen. Sobald es sich im Panel befindet, kannst du es verschieben und mit anderen Blöcken verbinden.

\--- /collapse \---

Wenn du sehen möchtest, was ein Block macht, kannst du ihn mit einem Doppelklick ausführen!

\--- task \--- Doppelklicke auf einige Blöcke, um zu sehen, was sie tun. \--- /task \---

## \--- collapse \---

## title: Den Code ausführen

Normalerweise soll dein Code automatisch ausgeführt werden, wenn etwas bestimmtes passiert. This is why many of your programs will start with a block from the **Events** category, most often this one:

```blocks3
    wenn die grüne flagge angeklickt
```

The code blocks connected to this block will run after the **green flag** is clicked.

Codeblöcke laufen von oben nach unten, daher ist die Reihenfolge wichtig, in der du deine Blöcke zusammenfügst. In diesem Beispiel `sagt` die Figur {:class="block3looks"} `Hallo!` bevor der `Miau` Ton {class="block3sound"} `abgespielt` wird.

```blocks3
    when green flag clicked
    say [Hello]
    play sound [meow v]
```

\--- /collapse \---

Removing or deleting code blocks you don’t want in your program is easy! Just drag them back into the code blocks palette.

**Be careful:** dragging them into the code blocks pallette will delete all the blocks connected to the block you drag, so make sure to separate code blocks you want to keep from those you want to remove. If you delete some code blocks by accident and want to get them back, right-click and then click on the **undo** option to get everything back.

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