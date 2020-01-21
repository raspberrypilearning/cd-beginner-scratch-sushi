## Mișcarea elementelor

În momentul de față, rechinul tău se mișcă în cerc și ar fi mult mai distractiv să fie controlat cu tastele săgeți. În acest card, vei învăța cum să faci asta!

\--- task \---

Start by deleting all code that you have for the shark.

\--- /task \---

As you’ve probably guessed, you’re going to need **Event** and **Motion** blocks again!

\--- task \---

This time, look for this block and drag it into the current sprite panel:

```blocks3
    când tasta [spațiu v] este apăsată
```

Click the little arrow (▼) beside `space`. You will see a list of all your keyboard keys that you can pick from.

\--- /task \---

You’re going to need four of the `when key pressed`{:class="block3events"} blocks — one for each of your arrow keys.

\--- task \---

To make your shark move, connect these blocks to **Motion** blocks like this:

```blocks3
    când tasta [săgeată stânga v] este apăsată
    mergi (-10) pași
```

```blocks3
    când tasta [săgeată dreapta v] este apăsată
    mergi (10) pași
```

```blocks3
    când tasta [săgeată în sus v] este apăsată
```

```blocks3
    când tasta [săgeată jos v] este apăsată
```

\--- /task \---

**Note**: `-10` means 'go back 10 steps'.

\--- task \---

Now click the green flag to test out your code.

\--- /task \---

Now your shark moves back and forwards, which is pretty cool, but it doesn’t move up or down. Also, if you look through the **Motion** blocks, you’ll see there are no blocks for 'up' or 'down'. There are a whole bunch of them related to **x** and **y** coordinates though — let's try those!

\--- task \---

Grab two `change y by`{:class="block3motion"} blocks, and update your code like this:

```blocks3
    când tasta [săgeată în sus v] este apăsată
+    modifică y cu (10)
```

```blocks3
    când tasta [săgeată jos v] este apăsată
+    modifică y cu (-10)
```

\--- /task \---

Now when you press the arrows keys, the shark moves all around the stage!

## \--- collapse \---

## title: Cum funcționează coordonatele x și y?

To talk about the positions of objects, such as sprites, we often use x- and y-coordinates. The **x-axis** of the Stage coordinate system runs from **left to right**, and the **y-axis** runs from **bottom to top**.

![](images/moving3.png)

A sprite can be located by the coordinates of its centre, for example `(15, -27)`, where `15` is its position along the x-axis , and `-27` its position along the y-axis.

+ Pentru a înțelege mai bine cum funcționează acest lucru, selectează un personaj și folosește comenzile **x** și **y** pentru a îl deplasa în interiorul scenei, setând diferite valori pentru coordonate.

![](images/xycoords.png)

+ Încearcă diferite perechi de valori pentru a vedea unde merge personajul! În Scratch, axa x merge de la `-240` la `240`, iar axa y merge de la `-180` la `180`.

\--- /collapse \---

### Repornirea jocului

The shark moves all over the screen now, but imagine this is a game: how do you restart it, and what happens at the start of each game?

You need to get the shark to its original location when the player starts the game. They'll start this game by clicking on the green flag, so you need to change the shark sprite's x- and y-coordinates when that happens.

That’s actually pretty easy! The centre of the stage is `(0, 0)` in `(x, y)` coordinates.

So all you need is an **Event** block for that green flag, and the **go to** block from **Motion**.

\--- task \---

Drag a `when green flag clicked`{:class="block3events"} **Event** block onto the current sprite panel.

```blocks3
    când se dă click pe stegulețul verde
```

Then find the `go to`{:class="block3motion"} **Motion** block, and attach it to your flag **Event** block.

```blocks3
    când se dă click pe stegulețul verde
+    mergi la x (0) y: (0)
```

Set the both the `x` and the `y` coordinate to `0` in the `go to`{:class="block3motion"} block if they are not already `0`.

\--- /task \---

\--- task \---

Now click the green flag: you should see the shark return to the centre of the stage!

\--- /task \---