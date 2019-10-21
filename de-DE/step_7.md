## Ferngesteuerte Fische

Ok, jetzt ist es Zeit, die Fische alleine zum Schwimmen zu bringen. Dazu benötigst du eine neue Art von Block: einen **Steuerungs** Block.

\--- Aufgabe \--- Wähle deine Fischfigur.

Ziehe eine `wenn grüne Flagge angeklickt`{:class="block3events"} **Ereignis-** - Block, ein `wiederhole fortlaufend`{:class="block3control"} **Steuerungs** - Block und einen `Gehe 10 Schritte`{:class=“block3motion"} **Beweguns-** Block in das **Figuren-Panel**wie folgt:

```blocks3
    Wenn die grüne Flagge angeklickt
    wiederhole fortlaufend 
       gehe (10) er Schritt
    ende
```

\--- /task \---

## \--- collapse \---

## Titel: Was macht der neue Block?

**Steuerungs** Blöcke bewirken, dass dein Programm eine bestimmte Anzahl oder unter bestimmten Bedingungen ausgeführt wird.

Hier macht der Fisch, was immer in dem `wiederhole fortlaufend`{:class="block3control"} - Block steht immer und immer wieder in einer Schleife. Wenn es also das letzte, was getan werden soll (Block) innerhalb des `wiederhole fortlaufend`{:class="block3control“} Blocks getan hat, beginnt es am Anfang von vorn und macht alles wieder, und so weiter.

\--- /collapse\---

\--- Aufgabe \--- Klicke jetzt auf die grüne Flagge und schau, was passiert! \--- /task \---

Nun, dieser Fisch stürzte gerade auf die Bühnenseite, und er bewegte sich viel zu schnell, als dass dein Hai ihn fangen könnte.

Zuerst musst du den Fisch verlangsamen. Das ist eigentlich ziemlich einfach, du musst nur eine Weile warten, nachdem du ihn 10 Schritte verschoben hast. Es gibt einen **Steuerungs** Block, der dir hier helfen wird:

```blocks3
    warte (1) sek
```

\--- task \--- Füge den `Warte`{:class="block3control"} - Block in deine Code innerhalb des `wiederhol fortlaufend`{:class="block3control"} - Blocks ein und ändere die Anzahl auf `0,5`, wie diese:

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

Die Zahl, die du im Block `Warte`{:class="block3control"} festgelegt hast, gibt an, wie viele **Sekunden** der Fisch warten soll. `0,5` ist eine halbe Sekunde.

Du kannst verschiedene Werte testen, um herauszufinden, welche für das Spiel am besten ist. Denke daran, dass du auch die Anzahl der Schritte innerhalb des Blocks `Gehe zu`{:class="block3motion"} - Blocks ändern kannst!

\--- /collapse \---

Der Fisch bewegt sich jetzt, aber du musst ihn auch vom Bühnenrand abprallen lassen. Dafür gibt es wieder einen **Bewegungs** Block!

\--- task \--- Suche den `Pralle vom Rand ab`{:class="block3motion"} - Block und füge ihn nach dem `Warte`{:class="block3control"} - Block hinzu. \--- /task \---

## \--- collapse \---

## Titel: Was macht der neue Block?

Der Block `Pralle am Rand ab`{:class="block3motion"} prüft, ob die Figur die Bühnenkante berührt, und dreht sich gegebenenfalls nach links, rechts, oben oder unten.

\--- /collapse \---

Natürlich wird dies zu einem umgekehrten Fisch führen, so dass du wieder einen `Setze Drehtyp`{:class="block3motion"} - Block benötigt.

\--- task \--- Aktualisiere deinen Code, um den Drehtyp des Fisches auf `links-rechts`{:class="block3motion"} am Anfang des Figurskripts festzulegen:

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

Der Fisch bewegt sich jetzt vorwärts und rückwärts, aber nur in einer geraden Linie - für den Spieler ein bisschen zu leicht mit dem Hai zu fangen! Du musst den Fisch weniger vorhersehbar machen.

Du weißt bereits aus einem vorherigen Schritt, wie du eine Figur drehen kannst, also beginne dort.

\--- Aufgabe \--- Füge den Schwimmanweisungen des Fisches eine Kurve hinzu und klicke auf die grüne Flagge.

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

Schon besser, aber noch zu vorhersehbar. Es muss zufälliger sein. Zum Glück kann Scratch das Zufällige für dich machen! Du benötigst nur eine neue Art von Block, den sogenannten **Operator-** Block.

## \--- collapse \---

## Titel: Was ist ein Operator?

**Operatoren** nehmen einen oder mehrere Werte auf (wie Zahlen, Text oder `True / False` Werte) und geben einen einzelnen Wert zurück. Den Wert, der zurückgegeben wird, kann man an der Form des Blocks erkennen: Runde Enden geben Zahlen oder Text, spitze Enden geben `Wahr / Falsch` zurück.

```blocks3
    (() + ())

   (verbinde [hallo] und [Welt])

   <[] = []>
```

\--- /collapse \---

\--- Aufgabe \--- Suche den `Zufallszahl-`{:class="block3operators"} **Operator-** Block, und schließe ihn mit einem Klick in die `Drehe um Grad`{:class="block3motion"} **Bewegungs-** Block an und ziehe es in das Feld, in dem du die Gradzahl festlegst.

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

**Hinweis**: Du kannst die minimalen und maximalen Werte ändern, die ausgewählt werden sollen, aber die Standardwerte (`1` und `10`) sind für dieses Spiel ziemlich gut.

Aufgabe Klicke auf die grüne Flagge, um den Code auszuführen! \--- /task \---

## \--- collapse \---

## Titel: Was macht nun der Wiederhole fortlaufend - Block?

Der Wiederhole fortlaufend-Block bewirkt, dass die Fischfigur vier Dinge in der folgender Reihenfolge ausführt:

1. Vorwärts gehen
2. Ein bisschen drehen
3. Kurz warten
4. Prüfen, ob es sich am Rand der Bühne befindet

Sobald die Figur die Prüfung ausgeführt hat, beginnt sie wieder am Anfang der Schleife und bewegt sich, dreht sich, wartet, überprüft, solange du dein Scratch-Programm ausführst.

\--- /collapse \---

Cool! Als nächstes: den Fisch fangen!