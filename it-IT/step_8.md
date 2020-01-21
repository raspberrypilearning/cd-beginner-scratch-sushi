## A pesca!

Lo squalo si muove, il pesce nuota, ma non interagiscon: se il pesce nuota direttamente nella bocca dello squalo, non succede nulla. È ora di cambiarlo!

Per prima cosa, devi verificare se il pesce sta toccando lo squalo. Per questo, avrai bisogno di un blocco **Controllo** e un blocco **Sensori**.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks3
    quando si clicca sulla bandiera verde
usa stile rotazione [left-right v]
per sempre 
  fai (10) passi
  ruota in senso orario di (numero a caso tra (1) e (10)) gradi
  attendi (0.5) secondi
  rimbalza quando tocchi il bordo
  + se <touching [Sprite1 v] ?> allora
  + end
end
```

\--- /task \---

## \--- collapse \---

## title: Come funziona?

The `if...then`{:class="block3control"} **Control** block needs to be given a `True/False` value.

**Sensing** blocks collect information, like where the sprite is, what it’s touching, etc. You're using this block:

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
    se <touching [Sprite1 v] ?> allora 
  + nascondi
end
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. That’s not great.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    quando si clicca sulla bandiera verde
+ mostra
usa stile rotazione [left-right v]
per sempre
end
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    rimbalza quando tocchi il bordo
se <touching [Sprite1 v] ?> allora 
  nascondi
  + attendi (1) secondi
  + vai a x: (numero a caso tra (-240) e (240)) y: (numero a caso tra (-180) e (180))
  + mostra
end
```

\--- /task \---

## \--- collapse \---

## title: Come funziona?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!