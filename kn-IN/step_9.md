## ಸ್ಕೋರ್ ಇಟ್ಟುಕೊಳ್ಳುವುದು

ಆಟಗಾರನು ಎಷ್ಟು ಮೀನುಗಳನ್ನು ಹಿಡಿಯುತ್ತಾನೆ ಎಂಬುದರ ಸ್ಕೋರ್ ಇರಿಸಿಕೊಳ್ಳಲು, ನಿಮಗೆ ಎಲ್ಲೋ ಸ್ಕೋರ್ ಅನ್ನು ಸಂಗ್ರಹಿಸುವ ಅಗತ್ಯವಿರುತ್ತದೆ, ಅದಕ್ಕೆ ಸೇರಿಸುವ ವಿಧಾನ ಮತ್ತು ಆಟವನ್ನು ಪುನರಾರಂಭಿಸಿದಾಗ ಅದನ್ನು ಮರುಹೊಂದಿಸುವ ವಿಧಾನ.

ಮೊದಲನೆಯದು: ಸ್ಕೋರ್ ಸಂಗ್ರಹಿಸುವುದು!

\--- task \---

Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

Enter `score` as the name.

![](images/catch6.png)

ನಿಮ್ಮ ಹೊಸ ವೇರಿಯಬಲ್ ಪರಿಶೀಲಿಸಿ!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## title: What are variables?

When you want to store information in a program, you use something called a **variable**. ಅದರ ಮೇಲೆ ಲೇಬಲ್ ಇರುವ ಪೆಟ್ಟಿಗೆಯಂತೆ ಯೋಚಿಸಿ: ನೀವು ಅದರಲ್ಲಿ ಏನನ್ನಾದರೂ ಹಾಕಬಹುದು, ಅದರಲ್ಲಿ ಏನಿದೆ ಎಂಬುದನ್ನು ಪರಿಶೀಲಿಸಬಹುದು ಮತ್ತು ಅದರಲ್ಲಿರುವುದನ್ನು ಬದಲಾಯಿಸಬಹುದು. You’ll find variables in the **Variables** section, but you need to create them first for them to show up there!

\--- /collapse \---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. ಎರಡನ್ನೂ ಮಾಡುವುದು ಬಹಳ ಸುಲಭ:

\--- task \---

From the **Variables** section, take the `set [my variable v] to [0]`{:class="block3variables"} and `change [my variable v] by [1]`{:class="block3variables"} blocks. Click on the little arrows in the blocks, choose `score` from the list, and then put the blocks into your program:

### ಶಾರ್ಕ್ಗಾಗಿ ಕೋಡ್

```blocks3
    when green flag clicked
+    set [score v] to [0]
    set rotation style [left-right v]
    go to x: (0) y: (0)
```

### Code for the fish

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

Cool! ಈಗ ನೀವು ಸ್ಕೋರ್ ಮತ್ತು ಎಲ್ಲವನ್ನೂ ಪಡೆದುಕೊಂಡಿದ್ದೀರಿ.