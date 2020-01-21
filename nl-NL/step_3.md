## Toevoegen en verwijderen van codeblokken

Geweldig! Je hebt je allereerste Scratch programma geschreven. Tijd om wat meer te leren over hoe je code in en uit Scratch kunt krijgen! Scratch code bestaat uit **blokken** zoals deze:

![](images/code1.png)

Je vindt alle blokken in het palet met **codeblokken**, onderverdeeld in verschillende categorieën op basis van wat ze doen.

## \--- collapse \---

## title: Gebruik blokken uit de verschillende categorieën

Klik op een categorienaam om de blokken in die categorie te bekijken. Hier is de **Beweging** categorie geselecteerd:

![](images/code2a.png)

Alle blokken in de categorie waarop je hebt geklikt, worden weergegeven in de lijst:

![](images/code2b.png)

Je kunt op het gewenste blok klikken en deze vervolgens naar het huidige sprite paneel slepen en loslaten. Zodra het in het paneel zit, kun je het verplaatsen en verbinden met andere blokken.

\--- /collapse \---

Als je wilt zien wat een blok doet, kun je erop dubbelklikken om het uit te laten voeren!

\--- task \---

Try double-clicking on some of the blocks to see what they do.

\--- /task \---

## \--- collapse \---

## title: De code uitvoeren

Usually, you want your code to run automatically whenever something specific happens. This is why many of your programs will start with a block from the **Events** category, most often this one:

```blocks3
    wanneer op groene vlag wordt geklikt
```

The code blocks connected to this block will run after the **green flag** is clicked.

Code blocks run from top to bottom, so the order in which you snap your blocks together matters. In this example, the sprite will `say`{:class="block3looks"} `Hello!` before it will `play`{:class="block3sound"} the `meow` sound.

```blocks3
    wanneer op groene vlag wordt geklikt
  zeg [Hallo]
  start geluid [meow v]
```

\--- /collapse \---

Removing or deleting code blocks you don’t want in your program is easy! Just drag them back into the code blocks palette.

**Be careful:** dragging them into the code blocks pallette will delete all the blocks connected to the block you drag, so make sure to separate code blocks you want to keep from those you want to remove. If you delete some code blocks by accident and want to get them back, right-click and then click on the **undo** option to get everything back.

![](images/code6.png)

\--- task \---

Try adding, deleting, and undeleting some code blocks!

\--- /task \---

### Alles bij elkaar brengen

Now you know how to move code around and make things happen, it's time for you to create a program to make the Scratch Cat walk in a circle!

\--- task \---

Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. You’ll find them in the **Events** and **Motion** lists.

```blocks3
    wanneer op groene vlag wordt geklikt
    neem [10] stappen
```

\--- /task \---

\--- task \---

Now, click on the green flag above the Stage.

![](images/code7.png)

\--- /task \---

You should see the cat walking in a straight line...not exactly what you want, right?

Note: If you click th flag too many times and the cat walks away, you can drag it back!

\--- task \---

Snap the turn block to the end to make the cat sprite walk in a circle. It’s in the **Motion** list too.

```blocks3
    wanneer op groene vlag wordt geklikt
   neem [10] stappen
+    draai cw (15) graden
```

\--- /task \---

## \--- collapse \---

## title: Hoe werkt draaien?

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. You can change that number, and the number of steps, by clicking on the number and typing in a new value.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Now save your work!

\--- /task \---