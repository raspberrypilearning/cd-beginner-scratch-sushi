## Controla al pez remotamente

Ok, es hora de hacer que el pez nade por sí mismo. Para ello, necesitarás un nuevo tipo de bloque: un bloque **Control**.

\--- task \---

Select your fish sprite.

Arrastra un bloque `al hacer clic en bandera verde`{:class="block3events"} de la categoría **Eventos**, un bloque `por siempre`{:class="block3control"} de la lista **Control**, y un bloque `mover 10 pasos`{:class="block3motion"} de la lista **Movimiento** al **panel del objeto**, así:

```blocks3
    al hacer clic en bandera verde
    por siempre
        mover (10) pasos
    end
```

\--- /task \---

## \--- collapse \---

## title: ¿Qué hace el nuevo bloque?

Los bloques de **Control** hacen que tu programa haga cosas un cierto número de veces, o bajo ciertas condiciones.

Aquí, el pez hace lo que está dentro del bloque `por siempre`{: class="block3control"} una y otra vez en un bucle infinito. Así que una vez que ha hecho la última cosa (bloque) dentro del bloque `por siempre`{:class="block3control"}, empieza en la parte superior y hace todo de nuevo, y así sucesivamente.

\--- /collapse \---

\--- task \---

Now click the green flag and watch what happens!

\--- /task \---

Bueno, ese pez se acaba de estrellar contra el borde del Escenario y además se movía demasiado rápido para que tu tiburón lo atrapara.

Primero, necesitas ralentizar el pez. En realidad es bastante fácil, solo necesitas esperar un poco después de que se mueva esos 10 pasos. Hay un bloque **Control** que te será de ayuda aquí:

```blocks3
    esperar (1) segundos
```

\--- task \---

Add the `wait`{:class="block3control"} block into your code inside the `forever`{:class="block3control"} block, and change the number to `0.5`, like this:

```blocks3
    al hacer clic en bandera verde
    por siempre
        mover (10) pasos
+      esperar (0.5) segundos
    end
```

\--- /task \---

## \--- collapse \---

## title: Haciendo ajustes

El número que estableces en el bloque `esperar`{:class="block3control"} dice cuántos **segundos** quieres que el pez espere. `0.5` es la mitad de un segundo.

Puedes probar diferentes valores para ver cuál es el mejor para el juego. Y recuerda que ¡también puedes cambiar el número de pasos dentro del bloque `mover`{:class="block3motion"}!

\--- /collapse \---

El pez se mueve ahora, pero también necesitas que rebote al tocar el borde del Escenario. ¡Una vez más, hay un bloque **Movimiento** para esto!

\--- task \---

Find the `if on edge bounce`{:class="block3motion"} block, and add it in after the `wait`{:class="block3control"} block.

\--- /task \---

## \--- collapse \---

## title: ¿Qué hace el nuevo bloque?

El bloque `si toca un borde, rebotar`{:class="block3motion"} comprueba si el sprite está tocando el borde del Escenario y, si es así, se gira a la izquierda, derecha, arriba o abajo como corresponda.

\--- /collapse \---

Por supuesto, esto hará que el pez nade al revés, así que necesitas otro bloque `fijar estilo de rotación a`{:class="block3motion"}.

\--- task \---

Update your code to set the rotation style of the fish to `left-right`{:class="block3motion"} at the beginning of the sprite's script:

```blocks3
    al hacer clic en bandera verde
+    fijar estilo de rotación a [izquierda-derecha v]
    por siempre
        mover (10) pasos
        esperar (0.5) segundos
        si toca un borde, rebotar
    end
```

\--- /task \---

El pez ahora se mueve hacia atrás y hacia adelante, pero solo en línea recta, ¡es demasiado fácil para que el jugador lo atrape con el tiburón! Necesitas hacer que el pez sea menos predecible.

Ya sabes por un paso anterior cómo hacer que un sprite gire, así que empieza por aquí.

\--- task \---

Add a turn into the fish's swimming instructions, and click the green flag.

```blocks3
    al hacer clic en bandera verde
    fijar estilo de rotación a [izquierda-derecha v]
    por siempre
        mover (10) pasos
+        girar a la derecha (10) grados
        esperar (0.5) segundos
        si toca un borde, rebotar
    end
```

\--- /task \---

Es mejor, pero todavía es demasiado predecible. Necesita ser más aleatorio. Afortunadamente, ¡Scratch puede aleatorizar por ti! Sólo necesitarás un nuevo tipo de bloque, llamado bloque **operador**.

## \--- collapse \---

## title: ¿Qué es un operador?

Los **Operadores** toman uno o más valores (como números, texto, o `Verdadero/Falso`) y devuelven un valor único. Puedes saber el tipo de valor que devolverá por la forma del bloque: los bloques de extremos redondos dan números o texto, los de extremos puntiagudos dan `Verdadero/Falso`.

```blocks3
    (() + ())

    (unir [hola ] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \---

Find the `pick random`{:class="block3operators"} **operator** block, and plug it into the `turn degrees`{:class="block3motion"} **Motion** block by clicking it and dragging it into the field where you set the number of degrees.

```blocks3
    al hacer clic en bandera verde
    fijar estilo de rotación a [izquierda-derecha v]
    por siempre
        mover (10) pasos
+        girar a la derecha (número aleatorio entre (1) y (10)) grados
        esperar (0.5) segundos
        si toca un borde, rebotar
    end
```

\--- /task \---

**Nota**: puedes cambiar los números mínimos y máximos, pero los valores por defecto (`1` y `10`) son bastante buenos para este juego, así que puede dejarlos.

\--- task \---

Click the green flag to run the code!

\--- /task \---

## \--- collapse \---

## title: Entonces, ¿qué hace ahora el bloque por siempre?

El bloque por siempre hace que el sprite del pez haga cuatro cosas en orden:

1. Avanzar
2. Girar un poco
3. Esperar brevemente
4. Comprobar si está en el borde del Escenario

Una vez que el sprite ha hecho la comprobación, comenzará al principio del bucle de nuevo y avanzará, girará, esperará, y comprobará, durante todo el tiempo que dejes tu programa de Scratch ejecutándose.

\--- /collapse \---

¡Genial! A continuación: ¡captura ese pez!