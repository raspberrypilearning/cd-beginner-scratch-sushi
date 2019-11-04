## Poruszanie rzeczami

W tej chwili twój rekin porusza się w kółko, ale kontrolowanie go za pomocą klawiszy strzałek byłoby o wiele przyjemniejsze. Na tej karcie dowiesz się, jak to zrobić!

\--- task \--- Zacznij od usunięcia całego kodu, który masz dla rekina. \--- /task \---

Jak pewnie się domyśliłaś, będziesz potrzebowała ponownie bloków **Zdarzenia** i **Ruch**!

\--- task \--- Tym razem poszukaj tego bloku i przeciągnij go do panelu bieżącego duszka:

```blocks3
    kiedy klawisz [spacja v] naciśnięty
```

Kliknij małą strzałkę (▼) obok `spacji`. Zobaczysz listę wszystkich klawiszy, które możesz wybrać. \--- /task \---

Będziesz potrzebowała czterech bloków `kiedy klawisz jest naciśnięty`{:class="block3events"} - po jednym dla każdego ze strzałek.

\--- task \--- Aby twój rekin się poruszył, połącz te bloki z blokami **Ruch** ten sposób:

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

**Uwaga**: `-10` oznacza „cofnij o 10 kroków”.

\--- task \--- Kliknij zieloną flagę, aby przetestować swój kod. \--- /task \---

Teraz twój rekin porusza się do tyłu i do przodu, co jest całkiem fajne, ale nie porusza się w górę ani w dół. Ponadto, jeśli spojrzysz na bloki **Ruch**, zobaczysz, że nie ma żadnych bloków dla ruchu „w górę” lub „w dół”. Istnieje jednak wiele związanych ze współrzędnymi **x** i **y** - spróbujmy je wykorzystać!

\--- task \--- Złap dwa bloki `zmień y o`{:class="block3motion"} i zaktualizuj swój kod tak:

```blocks3
    kiedy klawisz [strzałka w górę v] naciśnięty
+ zmień y o (10)
```

```blocks3
    kiedy klawisz [strzałka w dół v] naciśnięty
+ zmień y o (-10)
```

\--- /task \---

Teraz, gdy naciśniesz klawisze strzałek, rekin porusza się po scenie!

## \--- collapse \---

## title: Jak działają współrzędne X i Y?

Aby mówić o pozycjach obiektów, takich jak duszki, często używamy współrzędnych x i y. **Oś x** układu współrzędnych sceny biegnie od **lewej do prawej**, a **oś y** biegnie od **dołu do góry**.

![](images/moving3.png)

Duszek może być umieszczony za pomocą współrzędnych jego środka, na przykład `(15, -27)`, gdzie `15` jest jego pozycją wzdłuż osi x a `-27` to jego położenie wzdłuż osi y.

+ Aby przekonać się, jak to na prawdę działa, wybierz duszka i użyj elementów sterujących **x** i **y**, aby przesuwać go po scenie, ustawiając różne wartości współrzędnych.

![](images/xycoords.png)

+ Wypróbuj różne pary wartości, aby zobaczyć, gdzie idzie duszek! In Scratch, the x-axis goes from `-240` to `240`, and the y-axis goes from `-180` to `180`.

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