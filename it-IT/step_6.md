## Tutti gli sprite

Ora hai uno squalo che puoi muovere usando i tasti freccia. Bello! È ora di aggiungere del pesce da prendere.

\--- task \---

Fai clic sul pulsante **Scegli uno sprite** e, dalla schermata che apparirà, scegli un pesce.

![Il pulsante Scegli uno sprite](images/spritesNewFromLibrary.png)

Se il tuo pesce è un po' grande rispetto al tuo squalo, puoi usare il controllo delle dimensioni per rendere entrambi gli sprite della giusta misura!

![Controllo delle dimensioni dello sprite](images/sprites2.png)

Modificare il numero nel controllo della dimensione per rendere lo sprite più grande o più piccolo.

\--- /task \---

Grande! Successivamente, aggiungerai del codice per far muovere il pesce da solo, senza l'intervento del giocatore. Il tuo giocatore muoverà lo squalo e cercherà di catturare il pesce.

## \--- collapse \---

## title: che dire dello squalo in retromarcia?

Sembra un po' strano avere lo squalo che nuota all'indietro. Proprio come faresti tu girandoti piuttosto che camminando all'indietro, lo squalo si dovrebbe girerebbe invece che nuotare all'indietro. Fortunatamente per te, Scratch ha un blocco per questo!

Il blocco `punta in direzione`{:class="block3motion"} ti consente di scegliere la direzione verso cui punta lo sprite. Lo troverai nella sezione dei blocchi **Movimento**. Puoi digitare un numero qualsiasi di gradi, per puntare lo sprite dove vuoi.

\--- /collapse \---

\--- task \---

Grab a couple of copies of the `point in direction`{:class="block3motion"} block from the **Motion** list and connect them to your shark's code, like this:

```blocks3
    quando si preme il tasto [left arrow v]
+ punta in direzione (-90)
fai (10) passi
```

```blocks3
    quando si preme il tasto [right arrow v]
+ punta in direzione (90)
fai (10) passi
```

\--- /task \---

\--- task \---

Change the number of steps in the `move`{:class="block3motion"} blocks from `-10` to `10`.

If you try moving the shark around now after you've added the `point in direction`{:class="block3motion"} blocks, you might notice something a little strange happening. The shark may not be turning quite right!

![Upside down shark](images/spritesUpsideDown.png)

\--- /task \---

## \--- collapse \---

## title: Perché va sottosopra?

The problem here is that the shark sprite started, as all sprites do, with the 'all around' **rotation style**, and what you need it to have is the 'left-right' style.

As usual, there’s a block for that, and it’s in **Motion**!

\--- /collapse \---

\--- task \---

Look in the **Motion** category for the block `set rotation style`{:class="block3motion"}.

Add the block to your shark reset code from earlier, and set the rotation style to `left-right`{:class="block3motion"}, like this:

```blocks3
    quando si clicca sulla bandiera verde
+ usa stile rotazione [left-right v]
vai a x: (0) y: (0)
```

\--- /task \---