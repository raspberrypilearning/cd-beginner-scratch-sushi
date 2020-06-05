## Angeln!

Der Hai bewegt sich, der Fisch schwimmt, aber sie interagieren nicht: Wenn der Fisch direkt in den Mund des Hais schwimmt, passiert nichts. Zeit das zu ändern!

Zuerst musst du wissen, ob der Fisch den Hai berührt. Dazu benötigst du einen **Steuerungs** - Block und einen **Fühlen** - Block.

--- task ---

Füge den `wenn... dann`{:class="block3control"} **Steuerungs** Block innerhalb der `wiederhole fortlaufend`{:class="block3control"} -Schleife der Fischfigur unter dem `pralle am Rand ab`{:class="block3motion"} Block hinzu.

Ziehe den `wird berührt`{:class="block3sensing"} - Block in den oberen Bereich des `wenn... dann`{:class="block3control"} - Blocks, und klicke auf das kleine Dreieck, um den Namen der Hai-Figur auszuwählen. Wenn du es nicht geändert hast, wird es "Figur1" sein.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
+        if <touching [Sprite1 v] ?> then
    end
```

--- /task ---

--- collapse ---
---
title: Wie funktioniert das?
---
Der `wenn...dann`{:class="block3control"} **Steuerungs-** Block muss einen `Wahr / Falsch` Wert erhalten.

**Fühlen** - Blöcke sammeln Informationen, z.B. wo sich die Figur befindet, was sie berührt, usw. So verwendest du diesen Block:

```blocks3
    <touching [Sprite1 v] ?>
```

An den spitzen Enden dieses Blocks erkennst du, dass du den Wert `Wahr/Falsch` erhältst, den der `wenn...dann`{:class="block3control"} - Block benötigt.

--- /collapse ---

Natürlich hast du gerade einen `wenn...dann`{:class="block3control"} - Block hinzugefügt, ohne etwas für den 'dann' -Teil hinzuzufügen. Im Moment prüft dein Skript, ob die Fisch-Figur die Hai-Figur berührt, aber es gibt keine Reaktion darauf.

Du kannst den Fisch verschwinden lassen, als ob der Hai ihn gefressen hat, indem du den Block `versteck dich`{:class="block3looks"} verwendest.

--- task ---

Suche den Block `versteck dich`{:class="block3looks"} in der Liste **Aussehen** und füge ihm in den Block `wenn...dann`{:class="block3control"} so hinzu:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

--- /task ---

Sobald der Hai den Fisch fängt, verschwindet der Fisch endgültig. Das ist nicht so toll.

--- task ---

Setze den `zeige dich`{:class="block3looks"} -Block aus der **Aussehen**-Palette ganz an den Anfang des Fischcodes, damit du das Spiel zurücksetzen kannst.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

--- /task ---

Das ist schon besser, aber du möchtest nicht, dass der Spieler das Spiel jedes Mal neu starten muss, wenn er einen einzelnen Fisch fängt!

--- task ---

Aktualisiere den Code in deinem `falls...dann`{:class="block3control"} - Block, damit er so aussieht:

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

--- /task ---

--- collapse ---
---
title: Wie funktioniert das?
---

Du warst richtig clever: Wenn der Fisch versteckt ist, wartet er, bewegt sich und taucht wieder auf.

Es sieht so aus, als würden viele Fische erscheinen, aber es ist diese eine Figur, die sich bewegt!

--- /collapse ---

Das ist ein Spiel! Aber es gibt noch keine Möglichkeit, die Punkte zu zählen oder zu gewinnen. Das kannst du auch beheben - auf der nächsten Karte!