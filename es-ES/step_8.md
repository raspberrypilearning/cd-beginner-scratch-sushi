## ¡Pescando!

El tiburón se mueve, el pez nada, pero no interactúan: si el pez se desliza justo en la boca del tiburón, no pasa nada. ¡Es hora de cambiar eso!

Primero, necesitas saber si el pez está tocando al tiburón. Para esto, necesitarás un bloque **Control** y un bloque **Sensor**.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Arrastra el bloque `tocando...`{:class="block3sensing"} al espacio en la parte superior del bloque `si...entonces`{:class="block3control"} y haz clic en el pequeño triángulo para seleccionar el nombre del objeto tiburón. Si no lo has cambiado, será 'Sprite1'.

```blocks3
    al hacer clic en bandera verde
    fijar estilo de rotación a [izquierda-derecha v]
    por siempre
        mover (10) pasos
        girar a la derecha (número aleatorio entre (1) y (10)) grados
        esperar (0.5) segundos
        si toca un borde, rebotar
+        si <¿tocando [Sprite1 v] ?> entonces
    end
```

\--- /task \---

## \--- collapse \---

## title: ¿Cómo funciona?

El bloque **Control** `si...entonces`{:class="block3control"} debe recibir un valor `Verdadero/Falso`.

Los bloques **Sensores** recopilan información, como dónde está el objeto, qué está tocando, etc. Estás utilizando este bloque:

```blocks3
    <¿tocando [Sprite1 v] ?>
```

Por los bordes puntiagudos de este bloque, puedes saber que va a darte el valor `Verdadero/Falso` que el bloque `si...entonces`{:class="block3control"} necesita.

\--- /collapse \---

Por supuesto, acabas de añadir un bloque `si...entonces`{:class="block3control"} sin añadir nada para la parte 'entonces'. Así que en este momento tu código está comprobando si el objeto pez está tocando el objeto tiburón, pero no está haciendo nada en respuesta.

Puedes hacer que el pez desaparezca, como si el tiburón se lo comiera, usando el bloque `esconder`{:class="block3looks"}.

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    si <¿tocando [Sprite1 v] ?> entonces
+        esconder
    end
```

\--- /task \---

Ahora, una vez que el tiburón captura al pez, el pez desaparece para siempre. Esto no está bien.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    al hacer clic en bandera verde
+    mostrar
    fijar estilo de rotación [izquierda-derecha v]
    por siempre
```

\--- /task \---

Eso ya está mejor, ¡pero no quieres que el jugador tenga que reiniciar el juego cada vez que capture un pescado!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    si toca un borde, rebotar
    si <¿tocando [Sprite1 v] ?> entonces
        esconder
+        esperar (1) segundos
+        ir a x: (número aleatorio entre (-240) y (240)) y: (número aleatorio entre (-180) to (180))
+        mostrar
    end
```

\--- /task \---

## \--- collapse \---

## title: ¿Cómo funciona esto?

Aquí estás siendo inteligente: cuando el pescado está oculto, espera, se mueve y luego vuelve a aparecer.

Parece que muchos peces siguen apareciendo, ¡pero es el mismo objeto moviéndose de un lado a otro!

\--- /collapse \---

¡Eso es un juego! Pero todavía no hay manera de guardar la puntuación, o de ganar. También puedes arreglar eso: ¡en la siguiente tarjeta!