## Agregando y eliminando bloques de código

¡Genial! Has creado tu primer programa Scratch. ¡Es hora de aprender un poco más sobre cómo mover código dentro y fuera de Scratch! El código de Scratch se compone de **bloques** como estos:

![](images/code1.png)

Encontrarás todos los bloques en la **paleta de bloques de código**, ordenados en diferentes categorías de acuerdo con lo que hacen.

## \--- collapse \---

## title: Utilizando bloques de las diferentes categorías

Haz clic en el nombre de una categoría para ver los bloques en esa categoría. Aquí, la categoría **Movimiento** está seleccionada:

![](images/code2a.png)

Todos los bloques de la categoría en la que has hecho clic se muestran en una lista:

![](images/code2b.png)

Puedes hacer clic en el bloque que desees, y luego arrastrarlo al panel del objeto actual y soltarlo. Una vez que esté en el panel, puedes moverlo y conectarlo a otros bloques.

\--- /collapse \---

¡Si quieres ver lo que hace un bloque, puedes hacer doble clic en él para que se ejecute!

\--- task \---

Intenta hacer doble clic en algunos de los bloques para ver qué hacen.

\--- /task \---

## \--- collapse \---

## title: Ejecutando el código

Usually, you want your code to run automatically whenever something specific happens. Esta es la razón por la que muchos de tus programas comenzarán con un bloque de la categoría **Eventos**, normalmente este:

```blocks3
    al hacer clic en bandera verde
```

Los bloques de código conectados a este bloque se ejecutarán después de hacer clic en la **bandera verde**.

Code blocks run from top to bottom, so the order in which you snap your blocks together matters. En este ejemplo, el objeto va a `decir`{:class="block3looks"} `¡Hola!` antes que `iniciar`{:class="block3sound"} el sonido `meow`.

```blocks3
    when green flag clicked
    say [Hello]
    play sound [meow v]
```

\--- /collapse \---

¡Eliminar los bloques de código que no quieras en tu programa es fácil! Simplemente arrástralos de nuevo a la paleta de bloques de código.

**Be careful:** dragging them into the code blocks pallette will delete all the blocks connected to the block you drag, so make sure to separate code blocks you want to keep from those you want to remove. Si eliminas algunos bloques de código por accidente y deseas recuperarlos, haz clic con el botón derecho y luego haz clic en la opción **deshacer** para recuperar todo.

![](images/code6.png)

\--- task \---

¡Intenta agregar, eliminar y recuperar algunos bloques de código!

\--- /task \---

### Recapitulemos

Now you know how to move code around and make things happen, it's time for you to create a program to make the Scratch Cat walk in a circle!

\--- task \---

Asegúrate de tener el objeto del gato seleccionado en la lista de objetos, y luego arrastra los siguientes bloques al panel de objetos y conéctalos. Los encontrarás en las listas **Eventos** y **Movimiento**.

```blocks3
    al hacer clic en bandera verde
    mover [10] pasos
```

\--- /task \---

\--- task \---

Now, click on the green flag above the Stage.

![](images/code7.png)

\--- /task \---

Deberías ver al gato caminando en línea recta... esto no es exactamente lo que quieres, ¿verdad?

Nota: si haces clic en la bandera demasiadas veces y el gato se aleja, ¡puedes arrastrarlo hacia atrás!

\--- task \---

Snap the turn block to the end to make the cat sprite walk in a circle. It’s in the **Motion** list too.

```blocks3
    when green flag clicked
    move [10] steps
+    turn cw (15) degrees
```

\--- /task \---

## \--- collapse \---

## title: How does turning work?

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. You can change that number, and the number of steps, by clicking on the number and typing in a new value.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Now save your work!

\--- /task \---