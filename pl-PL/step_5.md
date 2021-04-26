## Poruszanie rzeczami

W tej chwili twój rekin porusza się w kółko, ale kontrolowanie go za pomocą klawiszy strzałek byłoby o wiele przyjemniejsze. Na tej karcie dowiesz się, jak to zrobić!

\--- task \---

Start by deleting all code that you have for the shark.

\--- /task \---

As you’ve probably guessed, you’re going to need **Event** and **Motion** blocks again!

\--- task \---

This time, look for this block and drag it into the current sprite panel:

```blocks3
    kiedy klawisz [spacja v] naciśnięty
```

Click the little arrow (▼) beside `space`. You will see a list of all your keyboard keys that you can pick from.

\--- /task \---

You’re going to need four of the `when key pressed`{:class="block3events"} blocks — one for each of your arrow keys.

\--- task \---

To make your shark move, connect these blocks to **Motion** blocks like this:

```blocks3
    kiedy klawisz [strzałka w lewo v] naciśnięty
    przesuń o (-10) kroków
```

```blocks3
    kiedy klawisz [strzałka w prawo v] naciśnięty
    przesuń o (10) kroków
```

```blocks3
    kiedy klawisz [strzałka w górę v] naciśnięty
```

```blocks3
    kiedy klawisz [strzałka w dół v] naciśnięty
```

\--- /task \---

**Note**: `-10` means 'go back 10 steps'.

\--- task \---

**Test:** Press the left arrow key and right arrow key multiple times to test your code.

\--- /task \---

Now your shark moves back and forwards, which is pretty cool, but it doesn’t move up or down. Also, if you look through the **Motion** blocks, you’ll see there are no blocks for 'up' or 'down'. There are a whole bunch of them related to **x** and **y** coordinates though — let's try those!

\--- task \---

Grab two `change y by`{:class="block3motion"} blocks, and update your code like this:

```blocks3
    kiedy klawisz [strzałka w górę v] naciśnięty
+ zmień y o (10)
```

```blocks3
    kiedy klawisz [strzałka w dół v] naciśnięty
+ zmień y o (-10)
```

\--- /task \---

Now when you press the arrows keys, the shark moves all around the stage!

## \--- collapse \---

## title: Jak działają współrzędne X i Y?

To talk about the positions of objects, such as sprites, we often use x- and y-coordinates. The **x-axis** of the Stage coordinate system runs from **left to right**, and the **y-axis** runs from **bottom to top**.

![](images/moving3.png)

A sprite can be located by the coordinates of its centre, for example `(15, -27)`, where `15` is its position along the x-axis , and `-27` its position along the y-axis.

+ Aby przekonać się, jak to na prawdę działa, wybierz duszka i użyj elementów sterujących **x** i **y**, aby przesuwać go po scenie, ustawiając różne wartości współrzędnych.

![](images/xycoords.png)

+ Wypróbuj różne pary wartości, aby zobaczyć, gdzie idzie duszek! W trybie Scratch oś X przechodzi od `-240` do `240`, a oś y wynosi od `-180` do `180`.

\--- /collapse \---

### Ponowne uruchomienie gry

The shark moves all over the screen now, but imagine this is a game: how do you restart it, and what happens at the start of each game?

You need to get the shark to its original location when the player starts the game. They'll start this game by clicking on the green flag, so you need to change the shark sprite's x- and y-coordinates when that happens.

That’s actually pretty easy! The centre of the stage is `(0, 0)` in `(x, y)` coordinates.

So all you need is an **Event** block for that green flag, and the **go to** block from **Motion**.

\--- task \---

Drag a `when green flag clicked`{:class="block3events"} **Event** block onto the current sprite panel.

```blocks3
    kiedy kliknięto zieloną flagę
```

Then find the `go to`{:class="block3motion"} **Motion** block, and attach it to your flag **Event** block.

```blocks3
    gdy flaga kliknięta
+ idź do x: (0) y: (0)
```

Set the both the `x` and the `y` coordinate to `0` in the `go to`{:class="block3motion"} block if they are not already `0`.

\--- /task \---

\--- task \---

Now click the green flag: you should see the shark return to the centre of the stage!

\--- /task \---