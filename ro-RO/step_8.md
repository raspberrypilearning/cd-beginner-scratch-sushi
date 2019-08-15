## La pescuit!

Rechinul se mișcă, peștele înoată, dar nu interacționează: dacă peștele înoată în gura rechinului, nu se întâmplă nimic. E timpul să schimbăm asta!

În primul rând, trebuie să verifici dacă peștele atinge rechinul. Pentru aceasta, vei avea nevoie de un bloc **Control** și un bloc **Detectare**.

\--- task \--- Adaugă blocul `dacă... atunci`{:class="block3control"} de tip **Control** în interiorul buclei `la infinit`{:class="block3control"} dedesubtul blocului `dacă atinge marginea, ricoșează`{:class="block3motion"} în codul peștelui.

Trage blocul `atinge...`{:class="block3sensing"} în spațiul din partea de sus a blocului `dacă...atunci`{:class="block3control"} și apasă pe triunghiul mic pentru a selecta numele personajului rechin. Dacă nu l-ai schimbat, va fi „Personaj1”.

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

Blocul `dacă...atunci`{:class="block3control"} de tip **Control** trebuie să primească o valoare `Adevărat/Fals`.

Blocurile **Detectare** colectează informații, cum ar fi în unde se află un personaj, ce lucruri atinge etc. Tu folosești acest bloc:

```blocks3
    <atinge [Personaj1 v]?>
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