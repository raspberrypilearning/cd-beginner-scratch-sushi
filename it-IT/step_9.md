## Keeping score

Per tenere il conto del numero di pesci catturati dal giocatore, avrai bisogno di un posto in cui memorizzare il punteggio, un modo per aggiungerlo e uno per reimpostarlo quando il gioco viene riavviato.

Primo: memorizzare il punteggio!

\--- task \--- Vai nella categoria dei blocchi **Variabili** e clicca su **Crea una variabile**.

![](images/catch5.png)

Inserisci `punteggio` come nome.

![](images/catch6.png)

Controlla la tua nuova variabile!

![La variabile Punteggio è visualizzata sulla scena](images/scoreVariableStage.png) \--- /task \---

## \--- collapse \---

## title: Cosa sono le variabili?

Quando vuoi memorizzare le informazioni in un programma, usi una cosa chiamata **variabile**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. Troverai le variabili nella sezione **Variabili**, ma devi prima crearle per farle apparire lì!

\--- /collapse \---

Ora devi aggiornare la variabile ogni volta che lo squalo mangia un pesce e ripristinarla quando il gioco viene riavviato. Fare entrambe le cose è abbastanza semplice:

\--- task \--- Dalla sezione **Variabili**, prendi i blocchi `porta [my variable v] a [0]`{:class="block3variables"} e `porta [my variable v] a [1]`{:class="block3variables"}. Fai clic sulle piccole frecce nei blocchi, scegli `punteggio` dall'elenco e quindi inserisci i blocchi nel tuo programma:

### Codice per lo squalo

```blocks3
    quando si clicca sulla bandiera verde
+ porta [score v] a [0]
usa stile rotazione [left-right v]
vai a x: (0) y: (0)
```

### Codice per il pesce

```blocks3
    if <touching [Sprite1 v] ?> then
+        change [score v] by [1]
        hide
        wait (1) secs
        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
        show
    end
```

\--- /task \---

Cool! Now you’ve got a score and everything.