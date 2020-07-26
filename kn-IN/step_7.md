## ರಿಮೋಟ್-ಕಂಟ್ರೋಲ್ ಮೀನು

ಸರಿ, ಈಗ ಮೀನುಗಳನ್ನು ಸ್ವಂತವಾಗಿ ಈಜುವಂತೆ ಮಾಡುವ ಸಮಯ ಬಂದಿದೆ. ಇದನ್ನು ಮಾಡಲು, ನಿಮಗೆ ಹೊಸ ರೀತಿಯ ಬ್ಲಾಕ್ ಅಗತ್ಯವಿರುತ್ತದೆ: **ನಿಯಂತ್ರಣ** ಬ್ಲಾಕ್.

\--- task \---

ನಿಮ್ಮ ಮೀನು sprite ಆಯ್ಕೆಮಾಡಿ.

`ಹಸಿರು ಧ್ವಜ ಕ್ಲಿಕ್ ಮಾಡಿದಾಗ` {:class="block3events"} **ಈವೆಂಟ್**ಬ್ಲಾಕ್ಅನ್ನು,`forever` {: class = "block3control"} **ನಿಯಂತ್ರಣ** ಬ್ಲಾಕ್ಅನ್ನು, ಮತ್ತು ` 10 ಹಂತಗಳನ್ನು ಸರಿಸಿ` {: class = "block3motion"} **ಮೋಶನ್** ಬ್ಲಾಕ್ಅನ್ನು**sprite ಪ್ಯಾನೆಲ್** ‌ ಗೆ ಎಳೆಯಿರಿ, ಹೀಗೆ:

```blocks3
    when green flag clicked
    forever
        move (10) steps
    end
```

\--- /task \---

## \--- collapse \---

## title: ಈ ಹೊಸ ಕೋಡ್ ಏನು ಮಾಡುತ್ತದೆ?

**ನಿಯಂತ್ರಣ** ಬ್ಲಾಕ್‌ಗಳು ನಿಮ್ಮ ಪ್ರೋಗ್ರಾಂ ಅನ್ನು ನಿರ್ದಿಷ್ಟ ಸಂಖ್ಯೆಯ ಬಾರಿ ಅಥವಾ ಕೆಲವು ಷರತ್ತುಗಳ ಅಡಿಯಲ್ಲಿ ಮಾಡುವಂತೆ ಮಾಡುತ್ತದೆ.

ಇಲ್ಲಿ, ಮೀನು `forever`{: class = "block3control"}ಬ್ಲಾಕ್ ಒಳಗೆ ಇರುವದನ್ನು ಲೂಪ್‌ನಲ್ಲಿ ಮತ್ತೆ ಮತ್ತೆ ಮಾಡುತ್ತದೆ, ಶಾಶ್ವತವಾಗಿ. ಆದ್ದರಿಂದ ಒಮ್ಮೆ ಅದು `forever`{: class = "block3control"} ಬ್ಲಾಕ್ ಒಳಗೆ ಕೊನೆಯ ಕೆಲಸವನ್ನು (ಬ್ಲಾಕ್) ಮಾಡಿದ ನಂತರ, ಅದು ಮೇಲ್ಭಾಗದಲ್ಲಿ ಪ್ರಾರಂಭವಾಗುತ್ತದೆ ಮತ್ತು ಎಲ್ಲವನ್ನೂ ಮತ್ತೆ ಮಾಡುತ್ತದೆ, ಮತ್ತು ಹೀಗೆ.

\--- /collapse \---

\--- task \---

ಈಗ ಹಸಿರು ಧ್ವಜವನ್ನು ಕೆಲವು ಬಾರಿ ಕ್ಲಿಕ್ ಮಾಡಿ ಮತ್ತು ಏನಾಗುತ್ತದೆ ಎಂಬುದನ್ನು ನೋಡಿ!

\--- /task \---

ಆದರೆ, ಆ ಮೀನು ಇವಾಗ ಸ್ಟೇಜ್ ನ ಬದಿಗೆ ಅಪ್ಪಳಿಸಿತು, ಮತ್ತು ಅದು ನಿಮ್ಮ ಶಾರ್ಕ್ ಹಿಡಿಯಲಾಗದಷ್ಟು ತುಂಬಾ ವೇಗವಾಗಿ ಚಲಿಸುತ್ತಿದೆ.

ಮೊದಲಿಗೆ, ನೀವು ಮೀನುಗಳನ್ನು ನಿಧಾನಗೊಳಿಸಬೇಕು. ಅದು ನಿಜಕ್ಕೂ ತುಂಬಾ ಸುಲಭ, ಅದು ಆ 10 ಹಂತಗಳನ್ನು ಚಲಿಸಿದ ನಂತರ ಸ್ವಲ್ಪ ಸಮಯ ಕಾಯುಬೇಕು. ** ಕಂಟ್ರೋಲ್ **ಬ್ಲಾಕ್ ಇಲ್ಲಿ ನಿಮಗೆ ಸಹಾಯ ಮಾಡುವುದು:

```blocks3
    wait (1) secs
```

\--- task \---

` ನಿರೀಕ್ಷಿಸಿ ` {:class="block3control"}ಬ್ಲಾಕ್ಅನ್ನು`forever`{:class="block3control"} ಬ್ಲಾಕ್ ಒಳಗೆ ಇರುವ ನಿಮ್ಮ ಕೋಡ್‌ಗೆ ಸೇರಿಸಿ, ಮತ್ತು ಸಂಖ್ಯೆಯನ್ನು `0.5` ಗೆ ಬದಲಾಯಿಸಿ, ಹೀಗೆ:

```blocks3
    when green flag clicked
    forever
        move (10) steps
+      wait (0.5) secs
    end
```

\--- /task \---

## \--- collapse \---

## title: ಹೊಂದಾಣಿಕೆಗಳನ್ನು ಮಾಡುವುದು

`wait` {: class = "block3control"} ಬ್ಲಾಕ್ನಲ್ಲಿ ನೀವು ಹೊಂದಿಸಿದ ಸಂಖ್ಯೆ ನೀವು ಎಷ್ಟು **ಸೆಕೆಂಡುಗಳು** ಮೀನು ಕಾಯಬೇಕೆಂದು ಬಯಸುತ್ತೀರಿ ಎಂದು ಹೇಳುತ್ತದ. `0.5` ಅರ್ಧ ಸೆಕೆಂಡ್.

ಆಟಕ್ಕೆ ಯಾವುದು ಉತ್ತಮ ಎಂದು ನೋಡಲು ನೀವು ವಿಭಿನ್ನ ಮೌಲ್ಯಗಳನ್ನು ಪರೀಕ್ಷಿಸಬಹುದು. ಮತ್ತು `move`{: class = "block3motion"} ಬ್ಲಾಕ್ ಒಳಗೆ ಕೂಡ ನೀವು ಹಂತಗಳ ಸಂಖ್ಯೆಯನ್ನು ಬದಲಾಯಿಸಬಹುದು ಎಂಬುದನ್ನು ನೆನಪಿಡಿ!

\--- /collapse \---

ಮೀನು ಈಗ ಚಲಿಸುತ್ತದೆ, ಆದರೆ ಸ್ಟೇಜ್ ನ ಅಂಚಿನಿಂದ ಬೌನ್ಸ್ ಆಗಬೇಕಿದೆ. ಮತ್ತೊಮ್ಮೆ, ** Motion**ಬ್ಲಾಕ್ ಇದಕ್ಕಾಗಿ ಇದೆ!

\--- task \---

`if on edge bounce`{: class = "block3motion"}ಬ್ಲಾಕ್ ಅನ್ನು ಹುಡುಕಿ, ಮತ್ತು `wait` {:class="block3control"}ಬ್ಲಾಕ್ನ ನಂತರ ಅದನ್ನು ಸೇರಿಸಿ.

\--- /task \---

## \--- collapse \---

## title: ಈ ಹೊಸ ಬ್ಲಾಕ್ ಏನು ಮಾಡುತ್ತದೆ?

`if on edge bounce` {:class="block3motion"}ಬ್ಲಾಕ್ sprite ಸ್ಟೇಜ್ನ ಅಂಚನ್ನು ಮುಟ್ಟುತ್ತಿದೆಯೇ ಎಂದು ಪರಿಶೀಲಿಸುತ್ತದೆ ಮತ್ತು ಅದು ಇದ್ದರೆ, ಅದು ಎಡಕ್ಕೆ, ಬಲಕ್ಕೆ, ಮೇಲಕ್ಕೆ ಅಥವಾ ಕೆಳಕ್ಕೆ ಸೂಕ್ತವಾಗಿ ತಿರುಗುತ್ತದೆ.

\--- /collapse \---

ಸಹಜವಾಗಿ, ಇದು ತಲೆಕೆಳಗಾಗಿರುವ ಮೀನುಗಳಿಗೆ ಕಾರಣವಾಗುತ್ತದೆ, ಆದ್ದರಿಂದ ನಿಮಗೆ `set rotation style` {: class = "block3motion"}ಬ್ಲಾಕ್ ಮತ್ತೆ ಬೇಕಾಗುತ್ತದೆ.

\--- task \---

ಮೀನಿನ ತಿರುಗುವಿಕೆಯ ಶೈಲಿಯನ್ನು ` ಎಡ-ಬಲಕ್ಕೆ`{:class="block3motion"} ಹೊಂದಿಸಲು ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು sprite‌ನ ಆರಂಭದಲ್ಲಿ ನವೀಕರಿಸಿ:

```blocks3
    when green flag clicked
+    set rotation style [left-right v]
    forever
        move (10) steps
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

ಮೀನು ಈಗ ಹಿಂದಕ್ಕೆ ಮತ್ತು ಮುಂದಕ್ಕೆ ಚಲಿಸುತ್ತದೆ, ಆದರೆ ಸರಳ ರೇಖೆಯಲ್ಲಿ ಮಾತ್ರ - ಆಟಗಾರನಿಗೆ ಶಾರ್ಕ್ ಹಿಡಿಯಲು ಸ್ವಲ್ಪ ಸುಲಭ! ನೀವು ಮೀನುಗಳನ್ನು ಕಡಿಮೆ ಪ್ರೆಡಿಕ್ಟಾಬಲ್ ಆಗಿಸಬೇಕು.

Sprite ತಿರುವು ಹೇಗೆ ಮಾಡಬೇಕೆಂದು ಹಿಂದಿನ ಹಂತದಿಂದ ನಿಮಗೆ ಈಗಾಗಲೇ ತಿಳಿದಿದೆ, ಆದ್ದರಿಂದ ಅಲ್ಲಿಂದ ಪ್ರಾರಂಭಿಸಿ.

\--- task \---

ಮೀನಿನ ಈಜು ಸೂಚನೆಗಳಿಗೆ ತಿರುವು ಸೇರಿಸಿ, ಮತ್ತು ಹಸಿರು ಧ್ವಜವನ್ನು ಕ್ಲಿಕ್ ಮಾಡಿ.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever
        move (10) steps
+        turn cw (10) degrees
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

ಇದು ಉತ್ತಮವಾಗಿದೆ, ಆದರೆ ಇನ್ನೂ ಹೆಚ್ಚಿನ ಪ್ಯಾಟರ್ನ್ ಇದೆ. ಇದು ಹೆಚ್ಚು ರಿಯಾಂಡಮ್ ಆಗಿರಬೇಕು. ಅದೃಷ್ಟವಶಾತ್, ಸ್ಕ್ರ್ಯಾಚ್ ನಿಮಗಾಗಿ ರಿಯಾಂಡಮ್ ಮಾಡಬಹುದು! ನಿಮಗೆ ** ಆಪರೇಟರ್**ಬ್ಲಾಕ್ ಎಂದು ಕರೆಯಲ್ಪಡುವ ಹೊಸ ರೀತಿಯ ಬ್ಲಾಕ್ ಅಗತ್ಯವಿದೆ.

## \--- collapse \---

## title: ಆಪರೇಟರ್ ಎಂದರೇನು?

** ಆಪರೇಟರ್ಸ್** ಒಂದು ಅಥವಾ ಹೆಚ್ಚಿನ ಮೌಲ್ಯಗಳನ್ನು ತೆಗೆದುಕೊಳ್ಳಿ (ಸಂಖ್ಯೆಗಳು, ಪಠ್ಯ ಅಥವಾ ` ನಿಜ / ತಪ್ಪು ` ಮೌಲ್ಯಗಳು) ಮತ್ತು ಒಂದೇ ಮೌಲ್ಯವನ್ನು ಮರಳಿ ನೀಡುತ್ತದೆ. ಬ್ಲಾಕ್ನ ಆಕಾರದಿಂದ ಅದು ಯಾವ ರೀತಿಯ ಮೌಲ್ಯವನ್ನು ನೀಡುತ್ತದೆ ಎಂದು ನೀವು ಹೇಳಬಹುದು: ಸುತ್ತಿನ ತುದಿಗಳು ಸಂಖ್ಯೆಗಳನ್ನು ಅಥವಾ ಪಠ್ಯವನ್ನು ನೀಡುತ್ತವೆ, ಪಾಯಿಂಟಿ ತುದಿಗಳು `ನಿಜ / ತಪ್ಪು`ನೀಡುತ್ತವೆ.

```blocks3
    (() + ())

    (join [hello ] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \---

Find the `pick random`{:class="block3operators"} **operator** block, and plug it into the `turn degrees`{:class="block3motion"} **Motion** block by clicking it and dragging it into the field where you set the number of degrees.

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
+        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
    end
```

\--- /task \---

**Note**: you can change the minimum and maximum numbers it will pick, but the default values (`1` and `10`) are pretty good for this game, so you can just leave them.

\--- task \---

ಕೋಡ್ ಅನ್ನು ಚಲಾಯಿಸಲು ಹಸಿರು ಧ್ವಜವನ್ನು ಕ್ಲಿಕ್ ಮಾಡಿ!

\--- /task \---

## \--- collapse \---

## title: So what does the forever block do now?

The forever block now makes the fish sprite do four things in order:

1. ಮುಂದೆ ಸರಿಸಿ
2. ಸ್ವಲ್ಪ ತಿರುಗಿ
3. ಸಂಕ್ಷಿಪ್ತವಾಗಿ ಕಾಯಿರಿ
4. Check whether it's at the edge of the Stage

Once the sprite has done the check, it will start at the beginning of the loop again and move, turn, wait, check, for as long as you let your Scratch program run.

\--- /collapse \---

Cool! ಮುಂದಿನದು: ಆ ಮೀನು ಹಿಡಿಯುವುದು!