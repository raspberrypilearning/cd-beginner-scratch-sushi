## La pescuit!

Rechinul se mișcă, peștele înoată, dar nu interacționează: dacă peștele înoată în gura rechinului, nu se întâmplă nimic. E timpul să schimbăm asta!

În primul rând, trebuie să verifici dacă peștele atinge rechinul. Pentru aceasta, vei avea nevoie de un bloc **Control** și un bloc **Detectare**.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks3
    când se dă click pe stegulețul verde
    setează stilul de rotație [left-right v]
    la infinit 
        mergi (10) pași
        rotește la dreapta (alege aleator între (1) și (10)) grade
        așteaptă (0.5) secunde
        dacă atinge marginea, ricoșează
+       dacă <atinge [Personaj1 v]?> atunci
    end
```

\--- /task \---

## \--- collapse \---

## title: Cum funcționează?

The `if...then`{:class="block3control"} **Control** block needs to be given a `True/False` value.

**Sensing** blocks collect information, like where the sprite is, what it’s touching, etc. You're using this block:

```blocks3
    <atinge [Personaj1 v]?>
```

From this block's pointy ends, you can tell it’s going to give you the `True/False` value that the `if...then`{:class="block3control"} block needs.

\--- /collapse \---

Of course, you’ve just added an `if...then`{:class="block3control"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

You can make the fish disappear, as if the shark ate it, by using the `hide`{:class="block3looks"} block.

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    dacă <atinge [Personaj1 v]?> atunci 
+        ascunde
end
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. That’s not great.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    când se dă click pe stegulețul verde
+    arată
    setează stilul de rotație [stânga-dreapta v]
    la infinit
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    dacă atinge marginea, ricoșează
    dacă <atinge [Personaj1 v]?> atunci 
        ascunde
+        așteaptă (1) secunde
+        mergi la x: (alege aleator între (-240) și (240)) y: (alege aleator între (-180) și (180))
+        arată
    end
```

\--- /task \---

## \--- collapse \---

## title: Cum funcționează?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!