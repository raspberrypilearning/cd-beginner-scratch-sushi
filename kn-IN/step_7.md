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

The number you set in the `wait`{:class="block3control"} block says how many **seconds** you want the fish to wait. `0.5` ಅರ್ಧ ಸೆಕೆಂಡ್.

ಆಟಕ್ಕೆ ಯಾವುದು ಉತ್ತಮ ಎಂದು ನೋಡಲು ನೀವು ವಿಭಿನ್ನ ಮೌಲ್ಯಗಳನ್ನು ಪರೀಕ್ಷಿಸಬಹುದು. And remember that you can change the number of steps inside the `move`{:class="block3motion"} block too!

\--- /collapse \---

The fish moves now, but you need it to bounce off the edge of the Stage too. Yet again, there’s a **Motion** block for this!

\--- task \---

Find the `if on edge bounce`{:class="block3motion"} block, and add it in after the `wait`{:class="block3control"} block.

\--- /task \---

## \--- collapse \---

## title: What does the new block do?

The `if on edge bounce`{:class="block3motion"} block checks if the sprite is touching the edge of the Stage and, if it is, it turns left, right, up, or down as appropriate.

\--- /collapse \---

Of course, this will lead to an upside-down fish, so you need a `set rotation style`{:class="block3motion"} block again.

\--- task \---

Update your code to set the rotation style of the fish to `left-right`{:class="block3motion"} at the beginning of the sprite's script:

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

The fish moves backwards and forwards now, but only in a straight line — a bit too easy for the player to catch with the shark! You need to make the fish less predictable.

You already know from a previous step how to make a sprite turn, so start there.

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

It’s better, but there’s still too much of a pattern. It needs to be more random. Luckily, Scratch can do random for you! You’ll just need a new kind of block, called an **operator** block.

## \--- collapse \---

## title: What's an operator?

**Operators** take in one or more values (like numbers, text, or `True/False` values) and give back a single value. You can tell the kind of value it will give back by the shape of the block: round ends give numbers or text, pointy ends give `True/False`.

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