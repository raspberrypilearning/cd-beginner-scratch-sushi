## Pêche!

Le requin bouge, le poisson nage, mais ils n'interagissent pas: si le poisson nage directement dans la bouche du requin, rien ne se passe. Il est temps de changer ça!

Tout d'abord, tu dois savoir si le poisson touche le requin. Pour cela, tu auras besoin d'un bloc **Contrôle** et d'un bloc **Détection**.

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

Drag the `touching...`{:class="block3sensing"} block into the space at the top of the `if...then`{:class="block3control"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks3
    lorsque le drapeau vert est cliqué
    définir style de rotation [gauche-droite v]
    répéter indéfiniment 
        déplacer de (10) pas
        tourner cw (choix aléatoire (1) à (10)) degrés
        attendre (0,5) secondes
        si sur le bord, rebondir
+ si <touching [Sprite1 v] ?> alors
    fin
```

\--- /task \---

## \--- collapse \---

## title: Comment ça marche?

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
    si <touching [Sprite1 v] ?> alors
+ cacher
    fin
```

\--- /task \---

Now once the shark catches the fish, the fish disappears for good. That’s not great.

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    lorsque le drapeau vert est cliqué
+ afficher
    définir style de rotation [gauche-droite v]
    répéter indéfiniment
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    si sur le bord, rebondir
    si <touching [Sprite1 v] ?> alors
        cacher
+ attendre (1) secondes
+ aller à x: (choisir au hasard (-240) à (240)) y: (choisir au hasard (-180) à (180))
+ montrer
    fin
```

\--- /task \---

## \--- collapse \---

## title: Comment ça marche?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!