## Alle sprites

Nu heb je een haai die je kunt laten bewegen met de pijltjestoetsen. Gaaf! Hoog tijd om wat vissen toe te voegen die hij kan vangen.

\--- task \---

Klik op de **Kies een sprite** knop en kies een vis uit het scherm dat geopend wordt.

![De Kies een sprite knop](images/spritesNewFromLibrary.png)

Als je vis een beetje groot is vergeleken met je haai, dan kun je Grootte gebruiken om beide sprites het juiste formaat te geven!

![Sprite grootte](images/sprites2.png)

Verander het getal achter Grootte om de sprite groter of kleiner te maken.

\--- /task \---

Geweldig! Later zul je code toevoegen om de vis zelfstandig te laten bewegen, zonder dat de speler helpt. Je speler zal de haai aansturen om te proberen de vis te vangen.

## \--- collapse \---

## title: Hoe zit het met de achterstevoren haai?

Het ziet er een beetje gek uit om de haai achterstevoren te laten zwemmen. Net zoals jij je liever omdraait in plaats van achteruit te lopen, wil de haai zich ook omdraaien in plaats van achterstevoren te zwemmen. Gelukkig heeft Scratch hier een blok voor!

Het `richt naar graden`{:class="block3motion"} blok laat je de richting bepalen waarnaar je sprite wijst. Je vindt het in de **Beweging** blokken categorie. Je kunt zelf het aantal graden bepalen om de sprite in de juiste richting te laten wijzen.

\--- /collapse \---

\--- task \---

Grab a couple of copies of the `point in direction`{:class="block3motion"} block from the **Motion** list and connect them to your shark's code, like this:

```blocks3
    wanneer [pijltje links v] is ingedrukt
+   richt naar (-90) graden
neem (10) stappen
```

```blocks3
    wanneer [pijltje rechts v] is ingedrukt
+   richt naar (90) graden
neem (10) stappen
```

\--- /task \---

\--- task \---

Change the number of steps in the `move`{:class="block3motion"} blocks from `-10` to `10`.

If you try moving the shark around now after you've added the `point in direction`{:class="block3motion"} blocks, you might notice something a little strange happening. The shark may not be turning quite right!

![Upside down shark](images/spritesUpsideDown.png)

\--- /task \---

## \--- collapse \---

## title: Waarom draait de haai ondersteboven?

The problem here is that the shark sprite started, as all sprites do, with the 'all around' **rotation style**, and what you need it to have is the 'left-right' style.

As usual, there’s a block for that, and it’s in **Motion**!

\--- /collapse \---

\--- task \---

Look in the **Motion** category for the block `set rotation style`{:class="block3motion"}.

Add the block to your shark reset code from earlier, and set the rotation style to `left-right`{:class="block3motion"}, like this:

```blocks3
    wanneer op de groene vlag wordt geklikt
+   maak draaistijl [links-rechts v]
ga naar x: (0) y: (0)
```

\--- /task \---