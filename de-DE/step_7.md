## Ferngesteuerte Fische

Ok, jetzt ist es Zeit, die Fische selbstständig schwimmen zu lassen. Dazu benötigst du eine neue Art von Block: einen **Steuerungs** Block.

\--- task \---

Wähle deine Fischfigur.

Ziehe eine `wenn grüne Flagge angeklickt`{:class="block3events"} **Ereignis**-Block, ein `wiederhole fortlaufend`{:class="block3control"} **Steuerungs**-Block und einen `Gehe 10 Schritte`{:class="block3motion"} **Bewegungs**-Block in das **Figuren-Panel** wie folgt:

```blocks3
    Wenn die grüne Flagge angeklickt
    wiederhole fortlaufend 
       gehe (10)  Schritte
    ende
```

\--- /task \---

## \--- collapse \---

## Titel: Was macht der neue Block?

**Steuerungs**-Blöcke bewirken, dass dein Programm eine bestimmte Anzahl wiederholt oder unter bestimmten Bedingungen ausgeführt wird.

Hier macht der Fisch, was immer in dem `wiederhole fortlaufend`{:class="block3control"}-Block steht immer und immer wieder in einer Schleife. Wenn es also das letzte Ding (Block), innerhalb des `wiederhole fortlaufend`{:class="block3control“} Blocks getan hat, beginnt es am Anfang von vorn und macht alles wieder, und so weiter.

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

Füge den `warte`{:class="block3control"}-Block in deinen Code innerhalb des `wiederhole fortlaufend`{:class="block3control"}-Blocks ein und ändere die Anzahl auf `0,5`, genau so:

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

Du kannst verschiedene Werte testen, um herauszufinden, welcher für das Spiel am besten ist. Denke daran, dass du auch die Anzahl der Schritte innerhalb des `gehe zu`{:class="block3motion"}-Blocks ändern kannst!

\--- /collapse \---

Der Fisch bewegt sich jetzt, aber du musst ihn auch vom Bühnenrand abprallen lassen. Dafür gibt es wieder einen **Bewegungs**-Block!

\--- task \---

Suche den `pralle vom Rand ab`{:class="block3motion"}-Block und füge ihn nach dem `warte`{:class="block3control"}-Block hinzu.

\--- /task \---

## \--- collapse \---

## Titel: Was macht der neue Block?

Der Block `pralle am Rand ab`{:class="block3motion"} prüft, ob die Figur die Bühnenkante berührt, und dreht sich gegebenenfalls nach links, rechts, oben oder unten.

\--- /collapse \---

Natürlich wird dies zu einem umgedrehten Fisch führen, so dass du wieder einen `setze Drehtyp`{:class="block3motion"}-Block benötigst.

\--- task \---

Aktualisiere deinen Code, um den Drehtyp des Fisches auf `links-rechts`{:class="block3motion"} am Anfang des Figurskripts festzulegen:

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

\--- task \---

Füge den Schwimmanweisungen des Fisches eine Drehung hinzu und klicke auf die grüne Flagge.

```blocks3
    Wenn die grüne Flagge angeklickt
   setze Drehtyp auf [left-right v]
   wiederhole fortlaufend 
      gehe (10) er Schritt
+        drehe dich nach rechts um (10) Grad im UZS
      warte (0.5) Sekunden
      pralle vom Rand ab
   Ende
```

\--- /task \---

Schon besser, aber noch zu vorhersehbar. Es muss zufälliger sein. Zum Glück kann Scratch das Zufällige für dich machen! Du benötigst nur eine neue Art von Block, den sogenannten **Operator**-Block.

## \--- collapse \---

## Titel: Was ist ein Operator?

**Operatoren** nehmen einen oder mehrere Werte auf (wie Zahlen, Text oder `Richtig/Falsch` Werte) und geben einen einzelnen Wert zurück. Den Wert, der zurückgegeben wird, kann man an der Form des Blocks erkennen: Runde Enden geben Zahlen oder Text, spitze Enden geben `Wahr/Falsch` zurück.

```blocks3
    (() + ())

   (verbinde [hallo] und [Welt])

   <[] = []>
```

\--- /collapse \---

\--- task \---

Suche den `Zufallszahl`{:class="block3operators"}-**Operator-**-Block und stecke ihn mit einem Klick in den `drehe um Grad`{:class="block3motion"} **Bewegungs**-Block und ziehe ihn in das Feld, in welchem du die Gradzahl festlegst.

```blocks3
    Wenn die grüne Flagge angeklickt
   setze Drehtyp auf [links-rechts v]
   wiederhole fortlaufend 
       gehe (10) er Schritt
+         drehe dich nach rechts um (Zufallszahl von (1) bis (10)) Grad
       warte (0.5) Sekunden
      pralle vom Rand ab
   Ende
```

\--- /task \---

**Hinweis**: Du kannst die minimalen und maximalen Werte ändern, die ausgewählt werden sollen, aber die Standardwerte (`1` und `10`) sind für dieses Spiel ziemlich gut.

\--- task \---

Klicke jetzt auf die grüne Flagge, um deinen Code zu auszuführen!

\--- /task \---

## \--- collapse \---

## Titel: Was macht nun der Wiederhole fortlaufend-Block?

Der 'wiederhole fortlaufend'-Block bewirkt, dass die Fischfigur vier Dinge in dieser Reihenfolge ausführt:

1. Vorwärts gehen
2. Ein bisschen drehen
3. Kurz warten
4. Prüfen, ob es sich am Rand der Bühne befindet

Sobald die Figur die Prüfung ausgeführt hat, beginnt sie wieder am Anfang der Schleife und bewegt sich, dreht sich, wartet, überprüft, solange du dein Scratch-Programm ausführst.

\--- /collapse \---

Cool! Als nächstes: den Fisch fangen!