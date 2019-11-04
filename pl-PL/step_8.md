## Łap rybę!

Rekin porusza się, ryba pływa, ale nie wchodzą w interakcję: jeśli ryba popłynie prosto w usta rekina, nic się nie stanie. Czas to zmienić!

Po pierwsze, musisz wiedzieć, czy ryba dotyka rekina. Do tego potrzebny jest blok z sekcji **Kontrola** i blok z sekcji **Czujniki**.

\--- task \--- Dodaj blok `jeżeli...to`{:class="block3control"} z sekcji **Kontrola** wewnątrz bloku pętli `zawsze`{:class="block3control"} dla duszka ryby, poniżej bloku `jeżeli na brzegu, odbij się`{:class="block3motion"}.

Przeciągnij blok `dotyka...`{:class="block3sensing"} do miejsca na górze bloku `jeżeli...to`{:class="block3control"} i kliknij mały trójkąt, aby wybrać nazwę duszka rekina. Jeśli go nie zmieniłaś, będzie to „rekin”.

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

Blok `jeżeli... to`{:class="block3control"} w sekcji **Kontrola** musi mieć wartość `Prawda/Fałsz`.

Bloki z sekcji **Czujniki** zbierają informacje, np. gdzie jest duszek, czego dotyka, itp. Używasz tego bloku:

```blocks3
    < dotyka [rekin v] ?>
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

Now once the shark catches the fish, the fish disappears for good. That’s not great.

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