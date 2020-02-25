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

¡Eliminar los bloques de código que no quieras en tu programa es fácil! Simplemente arrástralos de nuevo a la paleta de bloques de código.

**Ten cuidado:** al arrastrarlos a la paleta de bloques de códigos, se eliminarán todos los bloques conectados al bloque que arrastres, así que asegúrate de separar los bloques de códigos que quieres conservar de los que deseas eliminar. Si eliminas algunos bloques de código por accidente y deseas recuperarlos, haz clic con el botón derecho y luego haz clic en la opción **deshacer** para recuperar todo.

![](images/code6.png)

\--- task \---

Try adding, deleting, and undeleting some code blocks!

\--- /task \---

### Recapitulemos

Ahora que sabes cómo mover bloques de código y hacer que pasen cosas, ¡es hora de que crees un programa para que el gato camine en un círculo!

\--- task \---

Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. Los encontrarás en las listas **Eventos** y **Movimiento**.

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

Note: If you click the flag too many times and the cat walks away, you can drag it back!

\--- task \---

Snap the turn block to the end to make the cat sprite walk in a circle. Está en la lista **Movimiento** también.

```blocks3
    al hacer clic en bandera verde
    mover [10] pasos
+    girar a la derecha (15) grados
```

\--- /task \---

## \--- collapse \---

## title: ¿Cómo funciona el giro?

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. Puedes cambiar ese número y el número de pasos, haciendo clic en el número y escribiendo un nuevo valor.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Now save your work!

\--- /task \---