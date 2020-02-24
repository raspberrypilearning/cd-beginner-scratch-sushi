## Codeblöcke hinzufügen und entfernen

Großartig! Du hast dein allererstes Scratch-Programm geschrieben. Zeit, etwas mehr darüber zu lernen, wie Code in Scratch ein- und ausgeblendet wird! Der Scratch-Code besteht aus **Blöcken** wie diesen:

![](images/code1.png)

Du findest alle Blöcke in der **Codeblock-Palette**, sortiert nach verschiedenen Kategorien.

## \--- collapse \---

## title: Verwenden von Blöcken aus den verschiedenen Kategorien

Klicke auf einen Kategorienamen, um die Blöcke in dieser Kategorie anzuzeigen. Hier wird die Kategorie **Bewegung** ausgewählt:

![](images/code2a.png)

Alle Blöcke in der Kategorie, auf die du geklickt hast, werden in einer Liste angezeigt:

![](images/code2b.png)

Du kannst auf den gewünschten Block klicken, ihn dann in das aktuelle Figuren-Panel ziehen und loslassen. Sobald es sich im Panel befindet, kannst du es verschieben und mit anderen Blöcken verbinden.

\--- /collapse \---

Wenn du sehen möchtest, was ein Block macht, kannst du ihn mit einem Doppelklick ausführen!

\--- task \---

Versuche doppelt auf einige Blöcke zu klicken, um zu sehen, was sie tun.

\--- /task \---

## \--- collapse \---

## title: Den Code ausführen

Normalerweise soll dein Code automatisch ausgeführt werden, wenn etwas bestimmtes passiert. Aus diesem Grund beginnen viele deiner Programme mit einem Block aus der Kategorie **Ereignisse**, meistens dieser:

```blocks3
    wenn die grüne flagge angeklickt
```

Die mit diesem Block verbundenen Codeblöcke werden ausgeführt, nachdem die grüne **Flagge** angeklickt wurde.

Codeblöcke laufen von oben nach unten, daher ist die Reihenfolge wichtig, in der du deine Blöcke zusammenfügst. In diesem Beispiel `sagt` die Figur {:class="block3looks"} `Hallo!` bevor der `Miau` Ton {class="block3sound"} `abgespielt` wird.

```blocks3
    Wenn die grüne Flagge angeklickt
sage [Hallo]
spiele Klang [Miau v]
```

\--- /collapse \---

Das Entfernen oder Löschen von Codeblöcken, die du nicht in deinen Programm haben möchtest, ist einfach! Ziehe es einfach zurück in die Codeblock-Palette.

**Sei vorsichtig:** Wenn du sie in die Codeblock-Palette ziehst, werden alle Blöcke, die mit dem von dir gezogenen Block verbunden sind, gelöscht. Achte darauf, die Codeblöcke, die du entfernen möchtest, von denen zu trennen, welche du behalten möchtest. Wenn du einige Codeblöcke versehentlich gelöscht hast und sie zurückbekommen möchtest, klicke mit der rechten Maustaste, und klicke dann auf die Option **Rückgängig**, um alles wiederherzustellen.

![](images/code6.png)

\--- task \---

Versuche, einige Codeblöcke hinzuzufügen, zu löschen und wiederherzustellen!

\--- /task \---

### Alles zusammenfügen

Jetzt weißt du, wie du einen Code verschieben und Dinge in Bewegung setzen kannst. Jetzt ist es an der Zeit, ein Programm zu erstellen, mit dem die Scratch Katze im Kreis laufen kann!

\--- task \---

Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. You’ll find them in the **Events** and **Motion** lists.

```blocks3
    Wenn die grüne Flagge angeklickt
  gehe [10] er Schritt
```

\--- /task \---

\--- task \---

Now, click on the green flag above the Stage.

![](images/code7.png)

\--- /task \---

You should see the cat walking in a straight line...not exactly what you want, right?

Note: If you click the flag too many times and the cat walks away, you can drag it back!

\--- task \---

Snap the turn block to the end to make the cat sprite walk in a circle. It’s in the **Motion** list too.

```blocks3
    Wenn die grüne Flagge angeklickt
    gehe [10] er Schritt
+   drehe dich nach rechts um (15) Grad
```

\--- /task \---

## \--- collapse \---

## Titel: Wie funktioniert das Drehen?

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. You can change that number, and the number of steps, by clicking on the number and typing in a new value.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Now save your work!

\--- /task \---