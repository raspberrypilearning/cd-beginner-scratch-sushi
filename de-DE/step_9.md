## Mitzählen

Damit die Anzahl der Fische, die der Spieler fängt, erhalten bleibt, benötigst du eine Stelle, an der du die Punktezahl speichern kannst, eine Möglichkeit, sie zu erhöhen und sie zurückzusetzen, wenn das Spiel neu gestartet wird.

Erstens: Speichern der Punktzahl!

\--- task \---

Wechsle zur Kategorie **Variablen**-Blöcke und klicke auf **Variable erstellen**.

![](images/catch5.png)

Gib `Punkte` als Name ein.

![](images/catch6.png)

Überprüfe deine neue Variable!

![Die Punkte-Variable wird auf der Bühne angezeigt](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## Titel: Was sind Variablen?

Wenn du Informationen in einem Programm speichern möchtest, verwendest du eine sogenannte **Variable**. Stelle es dir vor wie eine Schachtel mit einem Etikett darauf: Du kannst etwas hineinlegen, prüfen, was darin ist, und ändern, was darin enthalten ist. Du findest Variablen im Abschnitt **Variablen**, aber du musst sie zuerst erstellen, damit sie dort angezeigt werden!

\--- /collapse \---

Jetzt musst du die Variable aktualisieren, wann immer der Hai einen Fisch frisst, und sie zurücksetzen, wenn das Spiel neu gestartet wird. Beides ist ziemlich einfach:

\--- task \---

Setze aus dem Abschnitt **Variablen** die `[Meine Variable v] auf [0]`{:class="block3variables"} und `ändere [Meine Variable v] um [1]`{:class="block3variables"} Blöcke. Klicke auf die kleinen Pfeile in den Blöcken, wähle `Punkte` aus der Liste und füge die Blöcke in dein Programm ein:

### Code für den Hai

```blocks3
    Wenn die grüne Flagge angeklickt
+     setze [Punkte v] auf [0]
   setze Drehtyp auf [links-rechts v]
   gehe zu x: (0) y: (0)
```

### Code für den Fisch

```blocks3
    falls <touching [Sprite1 v] ?>, dann 
+          ändere [Punkte v] um [1]
         verstecke dich
         warte (1) Sekunden
         gehe zu x: (Zufallszahl von (-240) bis (240)) y: (Zufallszahl von (-180) bis (180))
         zeige dich
   ende

```

\--- /task \---

Cool! Jetzt hast du eine Punktzahl und alles andere.