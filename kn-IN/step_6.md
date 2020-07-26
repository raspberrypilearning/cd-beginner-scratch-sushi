## ಎಲ್ಲಾ sprites

ಈಗ ನೀವು ಬಾಣದ ಕೀಲಿಗಳನ್ನು ಬಳಸಿ ಚಲಿಸಬಹುದಾದ ಶಾರ್ಕ್ ಅನ್ನು ಹೊಂದಿದ್ದೀರಿ. ಸೊಗಸಾಗಿದೆ! ಅದು ಹಿಡಿಯಲು ಕೆಲವು ಮೀನುಗಳನ್ನು ಸೇರಿಸುವ ಸಮಯ.

\--- task \---

Click the **New sprite** button, and on the screen that opens, choose a fish.

![The New sprite button](images/spritesNewFromLibrary.png)

If your fish is a bit big compared to your shark, you can use the size control to make both sprites the right size!

![Sprite size control](images/sprites2.png)

ಸ್ಪಿರಿಟ್ ಅನ್ನು ದೊಡ್ಡದಾಗಿ ಅಥವಾ ಚಿಕ್ಕದಾಗಿ ಮಾಡಲು ಗಾತ್ರ ನಿಯಂತ್ರಣದಲ್ಲಿ ಸಂಖ್ಯೆಯನ್ನು ಬದಲಾಯಿಸಿ.

\--- /task \---

ಅದ್ಭುತವಾಗಿದೆ! Later, you're going to add some code to make the fish move around on its own, without help from the player. ನಿಮ್ಮ ಆಟಗಾರನು ಶಾರ್ಕ್ ಅನ್ನು ಸರಿಸುತ್ತಾನೆ ಮತ್ತು ಮೀನು ಹಿಡಿಯಲು ಪ್ರಯತ್ನಿಸುತ್ತಾನೆ.

## \--- collapse \---

## title: What about the backwards shark?

ಆ ಶಾರ್ಕ್ ಹಿಂದಕ್ಕೆ ಈಜುವುದು ಸ್ವಲ್ಪ ತಮಾಷೆಯಾಗಿ ಕಾಣುತ್ತದೆ. ನೀವು ಸಾಮಾನ್ಯವಾಗಿ ಹಿಂದಕ್ಕೆ ನಡೆಯುವುದಕ್ಕಿಂತ ಹೆಚ್ಚಾಗಿ ತಿರುಗುವಂತೆಯೇ, ಶಾರ್ಕ್ ಹಿಂದಕ್ಕೆ ಈಜುವ ಬದಲು ತಿರುಗುತ್ತದೆ. Luckily for you, Scratch has a block for this!

The `point in direction`{:class="block3motion"} block lets you pick the direction your sprite is pointing in. You’ll find it in the **Motion** blocks section. You can type in any number of degrees, to point the sprite wherever you want.

\--- /collapse \---

\--- task \---

Grab a couple of copies of the `point in direction`{:class="block3motion"} block from the **Motion** list and connect them to your shark's code, like this:

```blocks3
    when [left arrow v] key pressed
+     point in direction (-90)
    move (10) steps
```

```blocks3
    when [right arrow v] key pressed
+     point in direction (90)
    move (10) steps
```

\--- /task \---

\--- task \---

Change the number of steps in the `move`{:class="block3motion"} blocks from `-10` to `10`.

If you try moving the shark around now after you've added the `point in direction`{:class="block3motion"} blocks, you might notice something a little strange happening. The shark may not be turning quite right!

![ತಲೆಕೆಳಗಾಗಿ ಶಾರ್ಕ್](images/spritesUpsideDown.png)

\--- /task \---

## \--- collapse \---

## title: Why does it go upside down?

The problem here is that the shark sprite started, as all sprites do, with the 'all around' **rotation style**, and what you need it to have is the 'left-right' style.

As usual, there’s a block for that, and it’s in **Motion**!

\--- /collapse \---

\--- task \---

Look in the **Motion** category for the block `set rotation style`{:class="block3motion"}.

Add the block to your shark reset code from earlier, and set the rotation style to `left-right`{:class="block3motion"}, like this:

```blocks3
    when green flag clicked
+     set rotation style [left-right v]
    go to x: (0) y: (0)
```

\--- /task \---