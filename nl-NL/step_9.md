## Score bijhouden

Om bij te houden hoeveel vissen de speler vangt, moet je iets hebben om de score in op te slaan, een manier om erbij op te tellen, en een manier om opnieuw te beginnen als het spel herstart wordt.

Ten eerste: de scoren opslaan!

\--- task \---

Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

Enter `score` as the name.

![](images/catch6.png)

Check out your new variable!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## title: Wat zijn variabelen?

When you want to store information in a program, you use something called a **variable**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. You’ll find variables in the **Variables** section, but you need to create them first for them to show up there!

\--- /collapse \---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. Doing both is pretty easy:

\--- task \---

From the **Variables** section, take the `set [my variable v] to [0]`{:class="block3variables"} and `change [my variable v] by [1]`{:class="block3variables"} blocks. Click on the little arrows in the blocks, choose `score` from the list, and then put the blocks into your program:

### Code voor de haai

```blocks3
    wanneer op groene vlag wordt gedrukt
+ maak [score v] [0]
maak draaistijl [links-rechts v]
ga naar x: (0) y: (0)
```

### Code voor de vis

```blocks3
    als <raak ik [Sprite1 v]> dan
+ verander [score v] met [1]
verdwijn
wacht (1) sec
ga naar x: (willekeurig getal tussen (-240) en (240)) y: (willekeurig getal tussen (-180) en (180))
verschijn
einde
```

\--- /task \---

Cool! Now you’ve got a score and everything.