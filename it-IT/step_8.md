## Fishing!

Lo squalo si muove, il pesce nuota, ma non interagiscon: se il pesce nuota direttamente nella bocca dello squalo, non succede nulla. È ora di cambiarlo!

Per prima cosa, devi verificare se il pesce sta toccando lo squalo. Per questo, avrai bisogno di un blocco **Controllo** e un blocco **Sensori**.

\--- task \--- Aggiungi il blocco **Controllo** `se... allora`{:class="block3control"} all'interno del ciclo `per sempre`{:class="block3control"} dello sprite del pesce, sotto il blocco `rimbalza quando tocchi il bordo`{:class="block3motion"}.

Trascina il blocco `sto toccando...`{:class="block3sensing"} dentro lo spazio nella parte superiore del blocco `se... allora`{:class="block3control"}, quindi fai clic sul piccolo triangolo per selezionare il nome dello sprite dello squalo. Se non lo hai cambiato, sarà "Sprite1".

```blocks3
    quando si clicca sulla bandiera verde
usa stile rotazione [left-right v]
per sempre 
  fai (10) passi
  ruota in senso orario di (numero a caso tra (1) e (10)) gradi
  attendi (0.5) secondi
  rimbalza quando tocchi il bordo
  + se <touching [Sprite1 v] ?> allora
  + end
end
```

\--- /task \---

## \--- collapse \---

## title: Come funziona?

Il blocco **Controllo** `se... allora`{:class="block3control"} deve ricevere un valore `True/False`.

I blocchi **Sensori** raccolgono informazioni, come per esempio dove si trova lo sprite, che cosa sta toccando, ecc. Stai usando questo blocco:

```blocks3
    <touching [Sprite1 v] ?>
```

Dall'aspetto a punta delle estremità di questo blocco, puoi capire subito che ti restituirà il valore `Vero/Falso` di cui ha bisogno il blocco `se... allora`{:class="block3control"}.

\--- /collapse \---

Naturalmente, hai appena aggiunto un blocco `se... allora`{:class="block3control"} senza aggiungere nulla per la parte "allora". Quindi al momento il tuo codice sta controllando se lo sprite pesce sta toccando lo sprite squalo, ma non sta fa accadere nulla in risposta.

Puoi far sparire il pesce, come se lo squalo lo mangiasse, usando il blocco `nascondi`{:class="block3looks"}.

\--- task \--- Cerca il blocco `nascondi`{: class = "block3looks"} nell'elenco **Aspetto** e inseriscilo all'interno del blocco `se... allora`{:class="block3control"}, in questo modo:

```blocks3
    se <touching [Sprite1 v] ?> allora 
  + nascondi
end
```

\--- /task \---

Ora, una volta che lo squalo cattura il pesce, il pesce scompare per sempre. Non è grandioso.

\--- task \--- Metti il blocco `mostra`{:class="block3looks"} da **Aspetto** all'inizio del codice fish, in modo da poter resettare il gioco.

```blocks3
    quando si clicca sulla bandiera verde
+ mostra
usa stile rotazione [left-right v]
per sempre
end
```

\--- /task \---

È già meglio, ma non vuoi che il giocatore debba riavviare il gioco ogni volta che cattura un solo pesce!

\--- task \--- Aggiorna il codice all'interno del tuo blocco `se... allora`{:class="block3control"} in questo modo:

```blocks3
    rimbalza quando tocchi il bordo
se <touching [Sprite1 v] ?> allora 
  nascondi
  + attendi (1) secondi
  + vai a x: (numero a caso tra (-240) e (240)) y: (numero a caso tra (-180) e (180))
  + mostra
end
```

\--- /task \---

## \--- collapse \---

## title: Come funziona?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!