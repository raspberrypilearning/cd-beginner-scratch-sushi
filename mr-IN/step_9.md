## Keeping score

To keep score of how many fish the player catches, you’ll need somewhere to store the score, a way of adding to it, and a way of resetting it when the game is restarted.

First: storing the score!

\--- task \---

Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

Enter `score` as the name.

![](images/catch6.png)

Check out your new variable!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## title: What are variables?

जेव्हा आपल्याला प्रोग्राममध्ये माहिती संचयित करायची असेल तर आपण ** variables ** वापरता. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. आपणास व्हेरिएबल्समध्ये **variables** विभागामध्ये आढळतील, परंतु त्यांना तेथे दर्शविण्यासाठी प्रथम आपण त्यांना तयार करणे आवश्यक आहे!

\--- /collapse \---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. Doing both is pretty easy:

\--- task \---

** veriables ** विभाग मधून, `set [my variable v] to [0]`{:class="block3variables"} आणि `change [my variable v] by [1]`{:class="block3variables"} ब्लॉक्स घ्या. ब्लॉक्समधील छोट्या बाणावर क्लिक करा, सूचीमधून ` score ` निवडा आणि नंतर आपल्या प्रोग्राममध्ये ते ब्लॉक्स ठेवा:

### Code for the shark

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

Cool! Now you’ve got a score and everything.