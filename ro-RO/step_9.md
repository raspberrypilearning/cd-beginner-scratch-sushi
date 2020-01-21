## Memorarea scorului

Pentru a ține minte câți pești a prins jucătorul ai nevoie de un loc în care să îl stochezi, o metodă de a adăuga la el și o metodă de a îl reseta atunci când se repornește jocul.

Primul lucru: stocarea scorului!

\--- task \---

Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

Enter `score` as the name.

![](images/catch6.png)

Check out your new variable!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## title: Ce sunt variabilele?

When you want to store information in a program, you use something called a **variable**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. You’ll find variables in the **Variables** section, but you need to create them first for them to show up there!

\--- /collapse \---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. Doing both is pretty easy:

\--- task \---

From the **Variables** section, take the `set [my variable v] to [0]`{:class="block3variables"} and `change [my variable v] by [1]`{:class="block3variables"} blocks. Click on the little arrows in the blocks, choose `score` from the list, and then put the blocks into your program:

### Cod pentru rechin

```blocks3
    când se dă click pe stegulețul verde
+    setează [scor v] la [0]
    setează stilul de rotație [stânga-dreapta v]
    mergi la x (0) y: (0)
```

### Cod pentru pește

```blocks3
    dacă <atinge [Personaj1 v]?> atunci 
+        schimbă [scor v] cu [1]
        ascunde
        așteaptă (1) secunde
        mergi la x: (alege aleator între (-240) și (240)) y: (alege aleator între (-180) și (180))
        arată
    end
```

\--- /task \---

Cool! Now you’ve got a score and everything.