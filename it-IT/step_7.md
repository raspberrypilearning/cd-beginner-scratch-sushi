## Pesce telecomandato

Ok, ora è il momento di far nuotare i pesci da soli. Per fare ciò, avrai bisogno di un nuovo tipo di blocco: un blocco **Controllo**.

\--- task \---

Seleziona il tuo sprite pesce.

Trascina un blocco `Situazioni` **quando si clicca sulla bandiera verde**{:class="block3events"}, un blocco `Controllo` **per sempre**{:class="block3control"} e un blocco `Movimento` **fai 10 passi**{:class="block3motion"} nel **pannello sprite**, in questo modo:

```blocks3
    quando si clicca sulla bandiera verde
per sempre 
  fai (10) passi
end
```

\--- /task \---

## \--- collapse \---

## title: Cosa fa il nuovo blocco?

I blocchi **controllo** fanno in modo che il programma esegua le operazioni un certo numero di volte o in determinate condizioni.

Qui, il pesce fa tutto ciò che si trova all'interno del blocco `per sempre`{:class="block3control"} all'infinito in modo ciclico, per sempre. Quindi, una volta eseguita l'ultima cosa (blocco) all'interno del blocco `per sempre`{:class="block3control"}, ricomincia da capo e fa di nuovo tutto, e così via.

\--- /collapse \---

\--- task \---

Ora clicca sulla bandiera verde e guarda cosa succede!

\--- /task \---

Bene, quel pesce si è schiantato sul lato della scena e si stava muovendo troppo velocemente perché il tuo squalo lo potesse catturare.

Per prima cosa, devi rallentare il pesce. In realtà è piuttosto semplice, ti basta solo aspettare un po' dopo averlo spostato di quei 10 passi. C'è un blocco **Controllo** che ti aiuterà in questo:

```blocks3
    attendi (1) secondi
```

\--- task \---

Aggiungi il blocco `attendi`{:class="block3control"} nel codice all'interno del blocco `per sempre`{:class="block3control"}, e modifica il numero a `0,5`, in questo modo:

```blocks3
    quando si clicca sulla bandiera verde
per sempre 
  fai (10) passi
  + attendi (0.5) secondi
end
```

\--- /task \---

## \--- collapse \---

## title: Apportare modifiche

Il numero impostato nel blocco `aspetta`{:class="block3control"} indica quanti **secondi** vuoi che il pesce attenda. `0,5` è mezzo secondo.

Puoi provare diversi valori per vedere qual è il migliore per il gioco. E ricorda che puoi modificare anche il numero di passi all'interno del blocco `fai...passi`{:class="block3motion"}!

\--- /collapse \---

Il pesce si sposta ora, ma è necessario che rimbalzi anche sul bordo della scena. Ancora una volta, c'è un blocco **Movimento** per questo!

\--- task \---

Trova il blocco `rimbalza quando tocchi il bordo`{:class="block3motion"} e aggiungilo dopo il blocco `attendi`{:class="block3control"}.

\--- /task \---

## \--- collapse \---

## title: Cosa fa il nuovo blocco?

Il blocco `rimbalza quando tocchi il bordo`{:class="block3motion"} controlla se lo sprite sta toccando il bordo della scena e, se succede, gira a sinistra, a destra, in alto o in basso a seconda dei casi.

\--- /collapse \---

Ovviamente, questo porterà a un pesce capovolto, quindi è necessario un blocco `usa stile di rotazione`{:class="block3motion"} di nuovo.

\--- task \---

Aggiorna il tuo codice per impostare lo stile di rotazione del pesce a `sinistra`{:class="block3motion"} all'inizio dello script dello sprite:

```blocks3
    quando si clicca sulla bandiera verde
+ usa stile rotazione [left-right v]
per sempre 
  fai (10) passi
  attendi (0.5) secondi
  rimbalza quando tocchi il bordo
end
```

\--- /task \---

Il pesce si muove avanti e indietro ora, ma solo in linea retta - catturarlo è un po' troppo facile per il giocatore squalo! Devi rendere il pesce meno prevedibile.

Sai già, da una fase precedente, come fare in modo che lo sprite curvi, quindi inizia da lì.

\--- task \---

Aggiungi un ruota alle istruzioni di nuoto del pesce e clicca sulla bandiera verde.

```blocks3
    quando si clicca sulla bandiera verde
usa stile rotazione [left-right v]
per sempre 
  fai (10) passi
  + ruota in senso orario di (10) gradi
  attendi (0.5) secondi
  rimbalza quando tocchi il bordo
end
```

\--- /task \---

È meglio, ma è ancora troppo schematico. Deve essere più casuale. Fortunatamente, Scratch può creare casualità per te! Avrai solo bisogno di un nuovo tipo di blocco, chiamato blocco **operatore**.

## \--- collapse \---

## title: Cos'è un operatore?

Gli **operatori** accettano uno o più valori (come numeri, testo o valori `True/False`) e ne restituiscono uno solo. Puoi capire il tipo di valore che restituirà dalla forma del blocco: le estremità arrotondate restituiscono numeri o testo, le estremità a punta `Vero/Falso`.

```blocks3
    (() + ())

    (join [hello] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \---

Trova il blocco `operatore` **numero a caso**{:class="block3operators"}, e collegalo al blocco `Movimento` **ruota**{:class="block3motion"} cliccandolo e trascinandolo nel punto in cui imposti il numero di gradi.

```blocks3
    quando si clicca sulla bandiera verde
usa stile rotazione [left-right v]
per sempre 
  fai (10) passi
  + ruota in senso orario di (numero a caso tra (1) e (10)) gradi
  attendi (0.5) secondi
  rimbalza quando tocchi il bordo
end
```

\--- /task \---

**Nota**: puoi cambiare i valori minimo e massimo tra cui sceglierà, ma i valori predefiniti (`1` e `10`) sono abbastanza buoni per questo gioco, quindi puoi lasciarli così.

\--- task \---

Fare clic sulla bandiera verde per eseguire il codice!

\--- /task \---

## \--- collapse \---

## title: Quindi cosa fa il blocco per sempre ora?

Il blocco per sempre ora fa in modo che lo sprite pesce faccia quattro cose in ordine:

1. Andare avanti
2. Girarsi un po '
3. Attendere brevemente
4. Controllare se ha raggiunto il bordo della scena

Una volta che lo sprite ha eseguito il controllo, inizierà di nuovo dall'inizio del ciclo e si sposterà, girerà, attenderà, verificherà, per tutto il tempo in cui il programma Scratch sarà in esecuzione.

\--- /collapse \---

Mitico! E adesso: catturiamo quel pesce!