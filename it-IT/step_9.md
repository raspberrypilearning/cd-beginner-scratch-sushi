## Tenere il punteggio

Per tenere il conto del numero di pesci catturati dal giocatore, avrai bisogno di un posto in cui memorizzare il punteggio, un modo per aggiungerlo e uno per reimpostarlo quando il gioco viene riavviato.

Primo: memorizzare il punteggio!

\--- task \---

Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

Enter `score` as the name.

![](images/catch6.png)

Check out your new variable!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## title: Cosa sono le variabili?

When you want to store information in a program, you use something called a **variable**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. You’ll find variables in the **Variables** section, but you need to create them first for them to show up there!

\--- /collapse \---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. Doing both is pretty easy:

\--- task \---

From the **Variables** section, take the `set [my variable v] to [0]`{:class="block3variables"} and `change [my variable v] by [1]`{:class="block3variables"} blocks. Click on the little arrows in the blocks, choose `score` from the list, and then put the blocks into your program:

### Codice per lo squalo

```blocks3
    quando si clicca sulla bandiera verde
+ porta [score v] a [0]
usa stile rotazione [left-right v]
vai a x: (0) y: (0)
```

### Codice per il pesce

```blocks3
    se <touching [Sprite1 v] ?> allora 
  + cambia [score v] di [1]
  nascondi
  attendi (1) secondi
  vai a x: (numero a caso tra (-240) e (240)) y: (numero a caso tra (-180) e (180))
  mostra
end
```

\--- /task \---

Cool! Now you’ve got a score and everything.