## Złap rybę!

Rekin porusza się, ryba pływa, ale nie wchodzą w interakcję: jeśli ryba popłynie prosto w usta rekina, nic się nie stanie. Czas to zmienić!

Po pierwsze, musisz wiedzieć, czy ryba dotyka rekina. Do tego potrzebny jest blok z sekcji **Kontrola** i blok z sekcji **Czujniki**.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw styl obrotu [lewo-prawo v]
    zawsze 
        przesuń o (10) kroków
        obróć w prawo o (losuj liczbę od (1) do (10)) stopni
        czekaj (0.5) sekund
        jeżeli na brzegu, odbij się
+        jeżeli < dotyka [rekin v] ?> to
    koniec
```

\--- /task \---

## \--- collapse \---

## title: Jak to działa?

The `if...then`{:class="block3control"} **Control** block needs to be given a `True/False` value.

**Sensing** blocks collect information, like where the sprite is, what it’s touching, etc. You're using this block:

```blocks3
    < dotyka [rekin v] ?>
```

From this block's pointy ends, you can tell it’s going to give you the `True/False` value that the `if...then`{:class="block3control"} block needs.

\--- /collapse \---

Of course, you’ve just added an `if...then`{:class="block3control"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

You can make the fish disappear, as if the shark ate it, by using the `hide`{:class="block3looks"} block.

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    jeżeli < dotyka [rekin v] ?> to
+        ukryj
    koniec
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. That’s not great.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    kiedy kliknięto zieloną flagę
+    pokaż
    ustaw styl obrotu [lewo-prawo v]
    zawsze
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    jeżeli na brzegu, odbij się
    jeżeli <dotyka [rekin v] ?> to 
        ukryj
+        czekaj (1) sekund
+        Idź do x: (losuj liczbę od (-240) do (240)) y: (losuj liczbę od (-180) do (180))
+        pokaż
    end
```

\--- /task \---

## \--- collapse \---

## title: Jak to działa?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!