## ಮೀನುಗಾರಿಕೆ!

ಶಾರ್ಕ್ ಚಲಿಸುತ್ತದೆ, ಮೀನು ಈಜುತ್ತದೆ, ಆದರೆ ಅವು ಇಂಟರಾಕ್ಟ್ ಮಾಡುವುದಿಲ್ಲ: ಮೀನುಗಳು ಶಾರ್ಕ್ ಬಾಯಿಗೆ ಸರಿಯಾಗಿ ಈಜಿದರೆ ಏನೂ ಆಗುವುದಿಲ್ಲ. ಅದನ್ನು ಬದಲಾಯಿಸುವ ಸಮಯ!

ಮೊದಲಿಗೆ, ಮೀನು ಶಾರ್ಕ್ ಅನ್ನು ಸ್ಪರ್ಶಿಸುತ್ತಿದೆಯೇ ಎಂದು ನೀವು ತಿಳಿದುಕೊಳ್ಳಬೇಕು. ಇದಕ್ಕಾಗಿ, ನಿಮಗೆ **ನಿಯಂತ್ರಣ** ಬ್ಲಾಕ್ ಮತ್ತು **ಸೆನ್ಸಿಂಗ್** ಬ್ಲಾಕ್ನ ಅಗತ್ಯವಿದೆ.

\--- task \---

` if...then ` {: class = "block3control"} **ನಿಯಂತ್ರಣ**ಬ್ಲಾಕ್ಅನ್ನು`forever`{: class = "block3control"} ಫಿಶ್ sprite‌ನ ಲೂಪ್ ಒಳಗೆ ಸೇರಿಸಿ, `if on edge bounce` {: class = "block3motion"} ಬ್ಲಾಕ್ನ ಕೆಳಗೆ.

`ಟಚಿಂಗ್...`{: class = "block3sensing"}ಬ್ಲಾಕ್ ಅನ್ನು `if...then`{:class="block3control"} ಬ್ಲಾಕ್ ನ ಮೇಲ್ಭಾಗದಲ್ಲಿರುವ ಜಾಗಕ್ಕೆ ಎಳೆಯಿರಿ, ಮತ್ತು ಶಾರ್ಕ್ spriteನ ಹೆಸರನ್ನು ಆಯ್ಕೆ ಮಾಡಲು ಚಿಕ್ಕ ತ್ರಿಕೋನವನ್ನು ಕ್ಲಿಕ್ ಮಾಡಿ. ನೀವು ಅದನ್ನು ಬದಲಾಯಿಸದಿದ್ದರೆ, ಅದು 'ಸ್ಪ್ರೈಟ್ 1' ಆಗಿರುತ್ತದೆ.

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

`if...then` {: class = "block3control"} **ನಿಯಂತ್ರಣ** ಬ್ಲಾಕ್ಗೆ `ನಿಜ / ತಪ್ಪು` ಮೌಲ್ಯ ನೀಡಬೇಕಾಗಿದೆ.

**ಸೆನ್ಸಿಂಗ್**ಬ್ಲಾಕ್sprite ಎಲ್ಲಿದೆ, ಅದು ಏನು ಸ್ಪರ್ಶಿಸುತ್ತಿದೆ ಇತ್ಯಾದಿಗಳಂತಹ ಮಾಹಿತಿಯನ್ನು ಸಂಗ್ರಹಿಸುತ್ತದೆ. ನೀವು ಈ ಬ್ಲಾಕ್ ಅನ್ನು ಬಳಸುತ್ತಿರುವಿರಿ:

```blocks3
    <touching [Sprite1 v] ?>
```

ಈ ಬ್ಲಾಕ್ನ ಪಾಯಿಂಟಿ ತುದಿಗಳಿಂದ, ಅದು ನಿಮಗೆ `ನಿಜ / ತಪ್ಪು` ಮೌಲ್ಯ ನೀಡಲಿದೆ ಎಂದು ನೀವು ಹೇಳಬಹುದು ಇದು `if...then` {: class = "block3control"} ಬ್ಲಾಕ್ನ ಅಗತ್ಯಗಳು.

\--- /collapse \---

ಖಂಡಿತ, ನೀವು ಈಗ ` if...then`{:class="block3control"}ಬ್ಲಾಕ್ ಅನ್ನು ಸೇರಿಸಿದ್ದೀರಿ ಅದೂ 'then' ಭಾಗಕ್ಕೆ ಏನನ್ನೂ ಸೇರಿಸದೆಯೇ. ಆದ್ದರಿಂದ ಈ ಸಮಯದಲ್ಲಿ ನಿಮ್ಮ ಸ್ಕ್ರಿಪ್ಟ್ ಮೀನು sprite ಶಾರ್ಕ್ sprite ಅನ್ನು ಸ್ಪರ್ಶಿಸುತ್ತಿದೆಯೇ ಎಂದು ಪರಿಶೀಲಿಸುತ್ತಿದೆ, ಆದರೆ ಇದು ಪ್ರತಿಕ್ರಿಯೆಯಾಗಿ ಏನನ್ನೂ ಆಗುತ್ತಿಲ್ಲ.

`ಮರೆಮಾಡು` {: class = "block3looks"} ಬ್ಲಾಕ್ಬಳಸಿ, ಶಾರ್ಕ್ ಅದನ್ನು ತಿನ್ನುತ್ತಿದ್ದಂತೆ ನೀವು ಮೀನು ಕಣ್ಮರೆಯಾಗಬಹುದು.

\--- task \---

`ಮರೆಮಾಡಿ` {:class="block3looks"}ಬ್ಲಾಕ್ಅನ್ನು ** Looks** ಪಟ್ಟಿಯಲ್ಲಿ ಹುಡುಕಿ, ಮತ್ತು ಅದನ್ನು `if...then`{: class "block3control"}ಬ್ಲಾಕ್ ಒಳಗೆ ಇರಿಸಿ, ಹಾಗೆ:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

\--- /task \---

ಈಗ ಒಮ್ಮೆ ಶಾರ್ಕ್ ಮೀನುಅನ್ನು ಹಿಡಿದರೆ, ಮೀನು ಶಾಶ್ವತವಾಗಿ ಕಣ್ಮರೆಯಾಗುತ್ತದೆ. ಅದು ದೊಡ್ಡದಲ್ಲ.

\--- task \---

`show`{: class = "block3looks"} ಬ್ಲಾಕ್ಅನ್ನು**Looks**ನಿಂದ ಮೀನು ಕೋಡ್ ನ ಪ್ರಾರಂಭದಲ್ಲಿಯೇ ಇರಿಸಿ, ಆದ್ದರಿಂದ ನೀವು ಆಟವನ್ನು ಮರುಹೊಂದಿಸಬಹುದು.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

\--- /task \---

ಅದು ಈಗಾಗಲೇ ಉತ್ತಮವಾಗಿದೆ, ಆದರೆ ಆಟಗಾರನು ಒಂದೇ ಮೀನು ಹಿಡಿದಾಗಲೆಲ್ಲ ಆಟವನ್ನು ಮರುಪ್ರಾರಂಭಿಸಬೇಕೆಂದು ನೀವು ಬಯಸುವುದಿಲ್ಲ!

\--- task \---

ನಿಮ್ಮ `if...then` {:class="block3control"}ಬ್ಲಾಕ್ನ ಒಳಗಿನ ಕೋಡ್ ಅನ್ನು ಈ ರೀತಿ ಕಾಣಲು ನವೀಕರಿಸಿ:

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