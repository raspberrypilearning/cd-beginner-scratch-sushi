## Moving things around

In questo momento il tuo squalo si muove in circolo, e sarebbe molto più divertente controllarlo con i tasti freccia. Con questa scheda, imparerai come farlo!

\--- task \--- Inizia cancellando tutto il codice che hai per lo squalo. \--- /task \---

Come probabilmente hai intuito, avrai di nuovo bisogno di **blocchi Situazioni** e **Movimento**!

\--- task \--- Questa volta, cerca questo blocco e trascinalo nel pannello dello sprite corrente:

```blocks3
    quando si preme il tasto [space v]
```

Fare clic sulla piccola freccia (▼) accanto alla parola `spazio`. Verrà visualizzato un elenco di tutti i tasti della tastiera tra cui è possibile scegliere. \--- /task \---

Avrai bisogno di quattro blocchi `quando si preme il tasto`{: class = "block3events"} - uno per ciascuno dei tasti freccia.

\--- task \--- Per far muovere il tuo squalo, collega questi altri blocchi al blocco **Movimento** come qui sotto illlustrato:

```blocks3
    quando si preme il tasto [left arrow v]
fai (-10) passi
```

```blocks3
    quando si preme il tasto [right arrow v]
fai (10) passi
```

```blocks3
    quando si preme il tasto [up arrow v]
```

```blocks3
    quando si preme il tasto [down arrow v]
```

\--- /task \---

**Nota**: `-10` significa 'indietro 10 passi'.

\--- task \--- Ora fai clic sulla bandiera verde per testare il tuo codice. \--- /task \---

Ora il tuo squalo si muove avanti e indietro, il che è abbastanza bello, ma non si muove su o giù. Inoltre, se guardi attraverso i blocchi **Movimento**, vedrai che non ci sono blocchi per "su" o "giù". There are a whole bunch of them related to **x** and **y** coordinates though — let's try those!

\--- task \--- Grab two `change y by`{:class="block3motion"} blocks, and update your code like this:

```blocks3
    when [up arrow v] key pressed
+     change y by (10)
```

```blocks3
    when [down arrow v] key pressed
+     change y by (-10)
```

\--- /task \---

Now when you press the arrows keys, the shark moves all around the stage!

## \--- collapse \---

## title: How do x- and y-coordinates work?

To talk about the positions of objects, such as sprites, we often use x- and y-coordinates. The **x-axis** of the Stage coordinate system runs from **left to right**, and the **y-axis** runs from **bottom to top**.

![](images/moving3.png)

A sprite can be located by the coordinates of its centre, for example `(15, -27)`, where `15` is its position along the x-axis , and `-27` its position along the y-axis.

+ To get a feel for how this actually works, select a sprite and use the **x** and **y** controls to move it around the stage by setting different values for the coordinates.

![](images/xycoords.png)

+ Try different pairs of values to see where the sprite goes! In Scratch, the x-axis goes from `-240` to `240`, and the y-axis goes from `-180` to `180`.

\--- /collapse \---

### Restarting the game

The shark moves all over the screen now, but imagine this is a game: how do you restart it, and what happens at the start of each game?

You need to get the shark to its original location when the player starts the game. They'll start this game by clicking on the green flag, so you need to change the shark sprite's x- and y-coordinates when that happens.

That’s actually pretty easy! The centre of the stage is `(0, 0)` in `(x, y)` coordinates.

So all you need is an **Event** block for that green flag, and the **go to** block from **Motion**.

\--- task \--- Drag a `when green flag clicked`{:class="block3events"} **Event** block onto the current sprite panel.

```blocks3
    when green flag clicked
```

Then find the `go to`{:class="block3motion"} **Motion** block, and attach it to your flag **Event** block.

```blocks3
    when green flag clicked
+     go to x: (0) y: (0)
```

Set the both the `x` and the `y` coordinate to `0` in the `go to`{:class="block3motion"} block if they are not already `0`.

\--- /task \---

\--- task \--- Now click the green flag: you should see the shark return to the centre of the stage! \--- /task \---