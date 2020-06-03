## Ferngesteuerte Fische

Ok, jetzt ist es Zeit, die Fische selbstständig schwimmen zu lassen. Dazu benötigst du eine neue Art von Block: einen **Steuerungs** Block.

\--- task \---

Wähle deine Fischfigur.

Ziehe eine `wenn grüne Flagge angeklickt`{:class="block3events"} **Ereignis-** - Block, ein `wiederhole fortlaufend`{:class="block3control"} **Steuerungs** - Block und einen `Gehe 10 Schritte`{:class=“block3motion"} **Bewegungs-** Block in das **Figuren-Panel** wie folgt:

```blocks3
    Wenn die grüne Flagge angeklickt
    wiederhole fortlaufend 
       gehe (10)  Schritte
    ende
```

\--- /task \---

## \--- collapse \---

## Titel: Was macht der neue Block?

**Steuerungs** Blöcke bewirken, dass dein Programm eine bestimmte Anzahl wiederholt oder unter bestimmten Bedingungen ausgeführt wird.

Hier macht der Fisch, was immer in dem `wiederhole fortlaufend`{:class="block3control"} - Block steht immer und immer wieder in einer Schleife. Wenn es also das letzte Ding (Block), innerhalb des `wiederhole fortlaufend`{:class="block3control“} Blocks getan hat, beginnt es am Anfang von vorn und macht alles wieder, und so weiter.

\--- /collapse \---

\--- task \---

Klicke jetzt auf die grüne Flagge und schau, was passiert!

\--- /task \---

Nun, dieser Fisch stürzte gerade auf die Bühnenseite und er bewegte sich viel zu schnell, als dass dein Hai ihn hätte fangen könnte.

Zuerst musst du den Fisch verlangsamen. Das ist eigentlich ziemlich einfach, du musst nur eine Weile warten, nachdem du ihn 10 Schritte verschoben hast. Es gibt einen **Steuerungs** Block, der dir hier helfen wird:

```blocks3
    warte (1) sek
```

\--- task \---

Füge den `warte`{:class="block3control"} - Block in deinen Code innerhalb des `wiederhole fortlaufend`{:class="block3control"} - Blocks ein und ändere die Anzahl auf `0,5`, genau so:

```blocks3
    Wenn die grüne Flagge angeklickt
    wiederhole fortlaufend 
        gehe (10) er Schritt
+      warte (0.5) Sekunden
    Ende
```

\--- /task \---

## \--- collapse \---

## Titel: Anpassungen vornehmen

Die Zahl, die du im Block `warte`{:class="block3control"} festgelegt hast, gibt an, wie viele **Sekunden** der Fisch warten soll. `0,5` ist eine halbe Sekunde.

Du kannst verschiedene Werte testen, um herauszufinden, welcher für das Spiel am besten ist. Denke daran, dass du auch die Anzahl der Schritte innerhalb des Blocks `gehe zu`{:class="block3motion"} - Blocks ändern kannst!

\--- /collapse \---

Der Fisch bewegt sich jetzt, aber du musst ihn auch vom Bühnenrand abprallen lassen. Dafür gibt es wieder einen **Bewegungs** Block!

\--- task \---

Suche den `pralle vom Rand ab`{:class="block3motion"} - Block und füge ihn nach dem `warte`{:class="block3control"} - Block hinzu.

\--- /task \---

## \--- collapse \---

## Titel: Was macht der neue Block?

Der Block `pralle am Rand ab`{:class="block3motion"} prüft, ob die Figur die Bühnenkante berührt, und dreht sich gegebenenfalls nach links, rechts, oben oder unten.

\--- /collapse \---

Natürlich wird dies zu einem umgekehrten Fisch führen, so dass du wieder einen `setze Drehtyp`{:class="block3motion"} - Block benötigst.

\--- task \---

Update your code to set the rotation style of the fish to `left-right`{:class="block3motion"} at the beginning of the sprite's script:

```blocks3
    Wenn die grüne Flagge angeklickt
+    setze Drehtyp auf [links-rechts v]
    wiederhole fortlaufend 
          gehe (10) er Schritt
          warte (0.5) Sekunden
          pralle vom Rand ab
    ende
```

\--- /task \---

The fish moves backwards and forwards now, but only in a straight line — a bit too easy for the player to catch with the shark! You need to make the fish less predictable.

You already know from a previous step how to make a sprite turn, so start there.

\--- task \---

Add a turn into the fish's swimming instructions, and click the green flag.

```blocks3
    Wenn die grüne Flagge angeklickt
   setze Drehtyp auf [left-right v]
   wiederhole fortlaufend 
      gehe (10) er Schritt
+        drehe dich nach rechts um (10) Grad
      warte (0.5) Sekunden
      pralle vom Rand ab
   Ende
```

\--- /task \---

It’s better, but there’s still too much of a pattern. It needs to be more random. Luckily, Scratch can do random for you! You’ll just need a new kind of block, called an **operator** block.

## \--- collapse \---

## Titel: Was ist ein Operator?

**Operators** take in one or more values (like numbers, text, or `True/False` values) and give back a single value. You can tell the kind of value it will give back by the shape of the block: round ends give numbers or text, pointy ends give `True/False`.

```blocks3
    (() + ())

   (verbinde [hallo] und [Welt])

   <[] = []>
```

\--- /collapse \---

\--- task \---

Find the `pick random`{:class="block3operators"} **operator** block, and plug it into the `turn degrees`{:class="block3motion"} **Motion** block by clicking it and dragging it into the field where you set the number of degrees.

```blocks3
    Wenn die grüne Flagge angeklickt
   setze Drehtyp auf [left-right v]
   wiederhole fortlaufend 
       gehe (10) er Schritt
+         drehe dich nach rechts um (Zufallszahl von (1) bis (10)) Grad
       warte (0.5) Sekunden
      pralle vom Rand ab
   Ende
```

\--- /task \---

**Note**: you can change the minimum and maximum numbers it will pick, but the default values (`1` and `10`) are pretty good for this game, so you can just leave them.

\--- task \---

Click the green flag to run the code!

\--- /task \---

## \--- collapse \---

## Titel: Was macht nun der Wiederhole fortlaufend - Block?

The forever block now makes the fish sprite do four things in order:

1. Vorwärts gehen
2. Ein bisschen drehen
3. Kurz warten
4. Prüfen, ob es sich am Rand der Bühne befindet

Once the sprite has done the check, it will start at the beginning of the loop again and move, turn, wait, check, for as long as you let your Scratch program run.

\--- /collapse \---

Cool! Next up: catching that fish!