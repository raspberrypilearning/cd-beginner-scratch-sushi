## ¡Pescando!

El tiburón se mueve, el pez nada, pero no interactúan: si el pez se desliza justo en la boca del tiburón, no pasa nada. ¡Es hora de cambiar eso!

Primero, necesitas saber si el pez está tocando al tiburón. Para esto, necesitarás un bloque **Control** y un bloque **Sensor**.

--- task ---

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
+        if <touching [Objeto1 v] ?> then
    end
```

--- /task ---

--- collapse ---
---
title: ¿Cómo funciona?
---

El bloque **Control** `si...entonces`{:class="block3control"} debe recibir un valor `Verdadero/Falso`.

Los bloques **Sensores** recopilan información, como dónde está el objeto, qué está tocando, etc. Estás utilizando este bloque:

```blocks3
    <touching [Objeto1 v] ?>
```

Por los bordes puntiagudos de este bloque, puedes saber que va a darte el valor `Verdadero/Falso` que el bloque `si...entonces`{:class="block3control"} necesita.

--- /collapse ---

Por supuesto, acabas de añadir un bloque `si...entonces`{:class="block3control"} sin añadir nada para la parte 'entonces'. Así que en este momento tu código está comprobando si el objeto pez está tocando el objeto tiburón, pero no está haciendo nada en respuesta.

Puedes hacer que el pez desaparezca, como si el tiburón se lo comiera, usando el bloque `esconder`{:class="block3looks"}.

--- task ---

Encuentra el bloque `esconder`{:class="block3looks"} en la lista **Apariencia**, y ponlo dentro del bloque `si...entonces`{:class="block3control"}, así:

```blocks3
    if <touching [Objeto1 v] ?> then
+        hide
    end
```

--- /task ---

Ahora, una vez que el tiburón captura al pez, el pez desaparece para siempre. Esto no está bien.

--- task ---

Arrastra el bloque `mostrar`{:class="block3looks"} desde la lista **Apariecia** al inicio del código del pez, para que puedas reiniciar el juego.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

--- /task ---

Eso ya está mejor, ¡pero no quieres que el jugador tenga que reiniciar el juego cada vez que capture un pescado!

--- task ---

Actualiza el código dentro de tu bloque `si...entonces`{:class="block3control"} para que quede así:

```blocks3
    if on edge, bounce
    if <touching [Objeto1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

--- /task ---

--- collapse ---
---
title: ¿Cómo funciona esto?
---

Aquí estás siendo inteligente: cuando el pescado está oculto, espera, se mueve y luego vuelve a aparecer.

Parece que muchos peces siguen apareciendo, ¡pero es el mismo objeto moviéndose de un lado a otro!

--- /collapse ---

¡Eso es un juego! Pero todavía no hay manera de guardar la puntuación, o de ganar. También puedes arreglar eso: ¡en la siguiente tarjeta!