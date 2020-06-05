## Mitzählen

Damit die Anzahl der Fische, die der Spieler fängt, erhalten bleibt, benötigst du eine Stelle, an der du die Punktezahl speichern kannst, eine Möglichkeit, sie zu erhöhen und sie zurückzusetzen, wenn das Spiel neu gestartet wird.

Erstens: Speichern der Punktzahl!

--- task ---

Wechsle zur Kategorie **Variablen** - Blöcke und klicke auf **Variable erstellen**.

![](images/catch5.png)

Gib `Punkte` als Name ein.

![](images/catch6.png)

Überprüfe deine neue Variable!

![Die Punkte-Variable wird auf der Bühne angezeigt](images/scoreVariableStage.png)

--- /task ---

--- collapse ---
---
title: Was sind Variablen?
---
Wenn du Informationen in einem Programm speichern möchtest, verwendest du eine sogenannte **Variable**. Stelle es dir vor wie eine Schachtel mit einem Etikett darauf: Du kannst etwas hineinlegen, prüfen, was darin ist, und ändern, was darin enthalten ist. Du findest Variablen im Abschnitt **Variablen**, aber du musst sie zuerst erstellen, damit sie dort angezeigt werden!

--- /collapse ---

Jetzt musst du die Variable aktualisieren, wann immer der Hai einen Fisch frisst, und sie zurücksetzen, wenn das Spiel neu gestartet wird. Beides zu tun ist ziemlich einfach:

--- task ---

Setze aus dem Abschnitt **Variablen** die `[Meine Variable v] auf [0]`{:class="block3variables"} und `ändere [Meine Variable v] um [1]`{:class="block3variables"} Blöcke. Klicke auf die kleinen Pfeile in den Blöcken, wähle `Punkte` aus der Liste und füge die Blöcke in dein Programm ein:

### Code für den Hai

```blocks3
    when green flag clicked
+    set [Punkte v] to [0]
    set rotation style [left-right v]
    go to x: (0) y: (0)
```

### Code für den Fisch

```blocks3
    if <touching [Sprite1 v] ?> then
+        change [Punkte v] by [1]
        hide
        wait (1) secs
        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
        show
    end

```

--- /task ---

Cool! Jetzt hast du eine Punktzahl und alles andere.