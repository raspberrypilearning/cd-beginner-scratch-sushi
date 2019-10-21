## Angeln!

Der Hai bewegt sich, der Fisch schwimmt, aber er interagiert nicht: Wenn der Fisch direkt in den Mund des Hais schwimmt, passiert nichts. Zeit das zu ändern!

First, you need to know if the fish is touching the shark. For this, you'll need a **Control** block and a **Sensing** block.

\--- task \--- Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
+        if <touching [Sprite1 v] ?> then
    end
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

\--- task \--- Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

\--- /task \---

Sobald der Hai den Fisch fängt, verschwindet der Fisch endgültig. Das ist nicht so toll.

\--- task \--- Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \--- Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

\--- /task \---

## \--- collapse \---

## title: How does this work?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!