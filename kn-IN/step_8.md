## ಮೀನುಗಾರಿಕೆ!

ಶಾರ್ಕ್ ಚಲಿಸುತ್ತದೆ, ಮೀನು ಈಜುತ್ತದೆ, ಆದರೆ ಅವು ಇಂಟರಾಕ್ಟ್ ಮಾಡುವುದಿಲ್ಲ: ಮೀನುಗಳು ಶಾರ್ಕ್ ಬಾಯಿಗೆ ಸರಿಯಾಗಿ ಈಜಿದರೆ ಏನೂ ಆಗುವುದಿಲ್ಲ. ಅದನ್ನು ಬದಲಾಯಿಸುವ ಸಮಯ!

ಮೊದಲಿಗೆ, ಮೀನು ಶಾರ್ಕ್ ಅನ್ನು ಸ್ಪರ್ಶಿಸುತ್ತಿದೆಯೇ ಎಂದು ನೀವು ತಿಳಿದುಕೊಳ್ಳಬೇಕು. ಇದಕ್ಕಾಗಿ, ನಿಮಗೆ **ನಿಯಂತ್ರಣ** ಬ್ಲಾಕ್ ಮತ್ತು **ಸೆನ್ಸಿಂಗ್** ಬ್ಲಾಕ್ನ ಅಗತ್ಯವಿದೆ.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. ನೀವು ಅದನ್ನು ಬದಲಾಯಿಸದಿದ್ದರೆ, ಅದು 'ಸ್ಪ್ರೈಟ್ 1' ಆಗಿರುತ್ತದೆ.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
+        if <touching [Sprite1 v] ?> then
    end
```

\--- /task \---

## \--- collapse \---

## title: ಇದು ಹೇಗೆ ಕೆಲಸ ಮಾಡುತ್ತದೆ?

The `if...then`{:class="block3control"} **Control** block needs to be given a `True/False` value.

**Sensing** blocks collect information, like where the sprite is, what it’s touching, etc. ನೀವು ಈ ಬ್ಲಾಕ್ ಅನ್ನು ಬಳಸುತ್ತಿರುವಿರಿ:

```blocks3
    <touching [Sprite1 v] ?>
```

From this block's pointy ends, you can tell it’s going to give you the `True/False` value that the `if...then`{:class="block3control"} block needs.

\--- /collapse \---

Of course, you’ve just added an `if...then`{:class="block3control"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

You can make the fish disappear, as if the shark ate it, by using the `hide`{:class="block3looks"} block.

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. ಅದು ದೊಡ್ಡದಲ್ಲ.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

\--- /task \---

## \--- collapse \---

## title: ಇದು ಹೇಗೆ ಕೆಲಸ ಮಾಡುತ್ತದೆ?

ನೀವು ಇಲ್ಲಿ ಬುದ್ಧಿವಂತರಾಗಿದ್ದೀರಿ: ಮೀನುಗಳನ್ನು ಮರೆಮಾಡಿದಾಗ ಅದು ಕಾಯುತ್ತದೆ, ಚಲಿಸುತ್ತದೆ ಮತ್ತು ನಂತರ ಮತ್ತೆ ತೋರಿಸುತ್ತದೆ.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

ಅದು ಆಟ! But there’s no way to keep score yet, or to win. ಅದನ್ನೂ ನೀವು ಸರಿಪಡಿಸಬಹುದು - ಮುಂದಿನ ಕಾರ್ಡ್‌ನಲ್ಲಿ!