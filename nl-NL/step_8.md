## Vissen!

De haai beweegt, de vis zwemt, maar ze reageren niet op elkaar: als de vis in de bek van de haai zwemt, gebeurt er niets. Hoog tijd om dat te veranderen!

Eerst moet je weten of de vis de haai aanraakt. Hiervoor heb je een **Besturen** blok en een **Waarnemen** blok nodig.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks3
    wanneer op de groene vlag wordt geklikt
maak draaistijl [links-rechts v]
herhaal
neem (10) stappen
draai cw (willekeurig getal tussen (1) en (10)) graden
wacht (0.5) sec
keer om aan de rand
+ als <touching [Sprite1 v] ?> dan
einde
```

\--- /task \---

## \--- collapse \---

## title: Hoe werkt het?

The `if...then`{:class="block3control"} **Control** block needs to be given a `True/False` value.

**Sensing** blocks collect information, like where the sprite is, what it’s touching, etc. You're using this block:

```blocks3
    <raak ik [Sprite1 v]>
```

From this block's pointy ends, you can tell it’s going to give you the `True/False` value that the `if...then`{:class="block3control"} block needs.

\--- /collapse \---

Of course, you’ve just added an `if...then`{:class="block3control"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

You can make the fish disappear, as if the shark ate it, by using the `hide`{:class="block3looks"} block.

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    als <raak ik [Sprite1 v]> dan
+ verdwijn
einde
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. That’s not great.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    wanneer op de groene vlag wordt geklikt
+ verschijn
maak draaistijl [links-rechts v]
herhaal
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    keer om aan de rand
als <touching [Sprite1 v] ?> dan
verdwijn
+ wacht (1) sec
+ ga naar x: (willekeurig getal tussen (-240) en (240)) y: (willekeurig getal tussen (-180) en (180))
+ verschijn
einde
```

\--- /task \---

## \--- collapse \---

## title: Hoe werkt dit?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!