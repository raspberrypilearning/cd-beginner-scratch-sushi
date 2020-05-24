## ¡Pescando!

El tiburón se mueve, el pez nada, pero no interactúan: si el pez se desliza justo en la boca del tiburón, no pasa nada. ¡Es hora de cambiar eso!

Primero, necesitas saber si el pez está tocando al tiburón. Para esto, necesitarás un bloque **Control** y un bloque **Sensor**.

\--- task \---

Agrega el bloque **Control** `si...entonces`{:class="block3control"} dentro del bucle `por siempre`{:class="block3control"} del sprite del pez, debajo del bloque `si toca un borde, rebotar`{:class="block3motion"}.

Arrastra el bloque `tocando...`{:class="block3sensing"} al espacio en la parte superior del bloque `si...entonces`{:class="block3control"} y haz clic en el pequeño triángulo para seleccionar el nombre del objeto tiburón. Si no lo has cambiado, será 'Sprite1'.

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

## title: ¿Cómo funciona?

El bloque **Control** `si...entonces`{:class="block3control"} debe recibir un valor `Verdadero/Falso`.

Los bloques **Sensores** recopilan información, como dónde está el objeto, qué está tocando, etc. Estás utilizando este bloque:

```blocks3
    <touching [Sprite1 v] ?>
```

Por los bordes puntiagudos de este bloque, puedes saber que va a darte el valor `Verdadero/Falso` que el bloque `si...entonces`{:class="block3control"} necesita.

\--- /collapse \---

Of course, you’ve just added an `if...then`{:class="block3control"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

You can make the fish disappear, as if the shark ate it, by using the `hide`{:class="block3looks"} block.

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. That’s not great.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

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