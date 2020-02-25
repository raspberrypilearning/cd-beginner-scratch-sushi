## Agregar y eliminar bloques de código

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

Try double-clicking on some of the blocks to see what they do.

\--- /task \---

## \--- collapse \---

## title: Ejecutando el código

Por lo general, quieres que tu código se ejecute automáticamente cada vez que sucede algo específico. Esta es la razón por la que muchos de tus programas comenzarán con un bloque de la categoría **Eventos**, con mayor frecuencia este:

```blocks3
    al hacer clic en bandera verde
```

Los bloques de código conectados a este bloque se ejecutarán después de hacer clic en la **bandera verde**.

Los bloques de código se ejecutan de arriba a abajo, por lo que es importante el orden en el que se juntan los bloques. En este ejemplo, el objeto`dirá`{: class = "block3looks"} `¡Hola!` antes de que se ejecute `{`: {= class = "block3sound"} el sonido `meow`.

```blocks3
    al hacer clic en bandera verde
    diga [Hello]
    reproducir sonido [miau v]
```

\--- /collapse \---

Removing or deleting code blocks you don’t want in your program is easy! Just drag them back into the code blocks palette.

**Be careful:** dragging them into the code blocks pallette will delete all the blocks connected to the block you drag, so make sure to separate code blocks you want to keep from those you want to remove. If you delete some code blocks by accident and want to get them back, right-click and then click on the **undo** option to get everything back.

![](images/code6.png)

\--- task \---

Try adding, deleting, and undeleting some code blocks!

\--- /task \---

### Putting it all together

Now you know how to move code around and make things happen, it's time for you to create a program to make the Scratch Cat walk in a circle!

\--- task \---

Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. You’ll find them in the **Events** and **Motion** lists.

```blocks3
    when green flag clicked
    move [10] steps
```

\--- /task \---

\--- task \---

Now, click on the green flag above the Stage.

![](images/code7.png)

\--- /task \---

You should see the cat walking in a straight line...not exactly what you want, right?

Note: If you click the flag too many times and the cat walks away, you can drag it back!

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