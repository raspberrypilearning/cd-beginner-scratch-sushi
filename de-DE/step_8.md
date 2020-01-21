## Angeln!

Der Hai bewegt sich, der Fisch schwimmt, aber er interagiert nicht: Wenn der Fisch direkt in den Mund des Hais schwimmt, passiert nichts. Zeit das zu ändern!

Zuerst musst du wissen, ob der Fisch den Hai berührt. Dazu benötigst du einen **Steuerungs** - Block und einen **Fühlen-** Block.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks3
    Wenn die grüne Flagge angeklickt
    setze Drehtyp auf [links-rechts v]
    wiederhole fortlaufend 
         gehe (10) er Schritt
         drehe dich nach rechts um (Zufallszahl von (1) bis (10)) Grad
         warte (0.5) Sekunden
         pralle vom Rand ab
+          falls <touching [Sprite1 v] ?>, dann
   Ende
```

\--- /task \---

## \--- collapse \---

## Titel: Wie funktioniert das?

The `if...then`{:class="block3control"} **Control** block needs to be given a `True/False` value.

**Sensing** blocks collect information, like where the sprite is, what it’s touching, etc. You're using this block:

```blocks3
    <touching [Sprite1 v] ?>
```

From this block's pointy ends, you can tell it’s going to give you the `True/False` value that the `if...then`{:class="block3control"} block needs.

\--- /collapse \---

Of course, you’ve just added an `if...then`{:class="block3control"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

You can make the fish disappear, as if the shark ate it, by using the `hide`{:class="block3looks"} block.

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    falls <touching [Sprite1 v] ?> , dann 
  + verstecke dich
ende
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. That’s not great.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    Wenn die grüne Flagge angeklickt
+   zeige dich
   setze Drehtyp auf [links-rechtst v]
   wiederhole fortlaufend
   Ende
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    pralle vom Rand ab
   falls <touching [Sprite1 v] ?>, dann 
      verstecke dich
+       warte (1) Sekunden
+       gehe zu x: (Zufallszahl von (-240) bis (240)) y: (Zufallszahl von (-180) bis (180))
+      zeige dich
   Ende
```

\--- /task \---

## \--- collapse \---

## Titel: Wie funktioniert das?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!