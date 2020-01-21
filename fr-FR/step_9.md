## Garder le score

Pour garder le score du nombre de poissons capturés par le joueur, tu as besoin d'un emplacement pour stocker le score, un moyen de l'ajouter et un moyen de le réinitialiser au redémarrage de la partie.

Premièrement: enregistrer le score!

\--- task \---

Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

Enter `score` as the name.

![](images/catch6.png)

Check out your new variable!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## title: Que sont les variables?

When you want to store information in a program, you use something called a **variable**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. You’ll find variables in the **Variables** section, but you need to create them first for them to show up there!

\--- /collapse \---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. Doing both is pretty easy:

\--- task \---

From the **Variables** section, take the `set [my variable v] to [0]`{:class="block3variables"} and `change [my variable v] by [1]`{:class="block3variables"} blocks. Click on the little arrows in the blocks, choose `score` from the list, and then put the blocks into your program:

### Code pour le requin

```blocks3
    lorsque le drapeau vert est cliqué 
+ définir [score v] sur [0]
    définir le style de rotation [gauche-droite v]
    passer à x: (0) y: (0)
```

### Code pour le poisson

```blocks3
    si <touching [Sprite1 v] ?> alors
+ changer [score v] par [1]
        masquer
        attendre (1) secondes
        aller à x: (choisir au hasard (-240) à (240)) y: (choisir au hasard (-180) à (180) )
        montrer
    fin
```

\--- /task \---

Cool! Now you’ve got a score and everything.