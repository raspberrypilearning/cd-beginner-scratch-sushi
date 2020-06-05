## Alle Figuren

Jetzt hast du einen Hai, den du mit den Pfeiltasten bewegen kannst. Klasse! Zeit, ein paar Fische hinzuzufügen, die er fangen kann.

--- task ---

Klicke auf die Schaltfläche **Neue Figur**, und wähle auf dem Bildschirm einen Fisch aus.

![Die Schaltfläche Neue Figur](images/spritesNewFromLibrary.png)

Wenn dein Fisch im Vergleich zu deinem Hai ein bisschen groß ist, kannst du mit der Größensteuerung beide Figuren auf die richtige Größe bringen!

![Einstellung der Figuren-Größe](images/sprites2.png)

Ändere die Zahl in der Größensteuerung, um die Figur größer oder kleiner zu machen.

--- /task ---

Großartig! Später fügst du Code hinzu, damit sich der Fisch ohne Hilfe des Spielers von alleine bewegen kann. Dein Spieler wird den Hai bewegen und versuchen, den Fisch zu fangen.

--- collapse ---
---
title: Was ist mit dem rückwärts schwimmenden Hai?
---

Es sieht ein bisschen komisch aus, wenn der Hai nach rückwärts schwimmt. So wie du dich normalerweise umdrehst anstatt rückwärts zu gehen, würde sich der Hai eher umdrehen als rückwärts zu schwimmen. Zum Glück hat Scratch dafür einen Block!

Mit dem `Drehe in Richtung`{:class="block3motion"} kannst du die Richtung auswählen, in die deine Figur zeigt. Du findest es im Bereich **Bewegung** Blöcke. Du kannst einen beliebigen Wert in Grad eingeben, um die Figur auszurichten, wie du möchtest.

--- /collapse ---

--- task ---

Nimm ein paar Kopien des `setze Richtung auf`{:class="block3motion"} - Blocks aus der **Bewegung**- Liste und verbinde sie mit dem Code deines Hais:

```blocks3
    when [left arrow v] key pressed
+     point in direction (-90)
    move (10) steps
```

```blocks3
    when [right arrow v] key pressed
+     point in direction (90)
    move (10) steps
```

--- /task ---

--- task ---

Ändere die Anzahl der Schritte in den Blöcken `Setze auf`{:class="block3motion"} von `-10` auf `10`.

Wenn du versuchst, den Hai jetzt zu verschieben, nachdem du den `Setze Richtung auf`{:class="block3motion"} hinzugefügt hast, stellst du möglicherweise etwas ungewöhnliches fest. Der Hai dreht sich möglicherweise nicht ganz richtig!

![Umgedrehter Hai](images/spritesUpsideDown.png)

--- /task ---

--- collapse ---
---
title: Warum steht es auf dem Kopf?
---

Das Problem hier ist, dass die Hai-Figur wie alle Figuren mit dem 'rundherum' **Drehtyp** begonnen hat, und was du brauchst, ist der 'links-rechts'-Drehtyp.

Wie üblich gibt es dafür einen Block und du findest ihn in **Bewegung**!

--- /collapse ---

--- task ---

Suche in der Kategorie **Bewegung** nach dem Block `für Drehtyp`{:class="block3motion"}.

Füge den Block zu deinem Hai-zurücksetzen-Code von vorhin hinzu und setze den Drehtyp auf `links-rechts`{:class="block3motion"}:

```blocks3
    when green flag clicked
+     set rotation style [left-right v]
    go to x: (0) y: (0)
```

--- /task ---