## Poisson télécommandé

D'accord, il est maintenant temps de faire nager le poisson tout seul. Pour ce faire, tu auras besoin d’un nouveau type de bloc: un bloc **Contrôle**.

\--- task \--- Sélectionne ton sprite poisson.

Fais glisser un bloc `lorsque le drapeau vert est cliqué`{:class="block3events"} **Événement**, un bloc `répéter indéfiniment`{: class = "block3control"} **Contrôle**, et un bloc `déplacement de 10 pas`{:class="block3motion"} **Mouvement** dans le **panneau sprite**, comme ceci:

```blocks3
    lorsque le drapeau vert est cliqué sur
    répéter indéfiniment
        déplacer de (10) pas
    fin
```

\--- /task \---

## \--- collapse \---

## title: que fait le nouveau bloc?

**Les blocs de contrôle** obligent ton programme à effectuer des tâches un certain nombre de fois ou dans certaines conditions.

Ici, le poisson fait ce qui est dans le bloc `répéter indéfiniment`{:class="block3control"} encore et encore sur une boucle, pour toujours. Ainsi, une fois la dernière chose (bloc) passée dans le bloc `répéter indéfiniment`{:class="block3control"}, il recommence en haut et fait de nouveau tout, et ainsi de suite.

\--- /collapse \---

\--- task \--- Maintenant, clique sur le drapeau vert et regarde ce qui se passe! \--- /task \---

Eh bien, ce poisson vient de s'écraser sur le côté de la scène et il se déplaçait beaucoup trop vite pour que ton requin puisse l'attraper.

Tout d'abord, tu dois ralentir le poisson. C'est en fait assez facile, tu as juste besoin d'attendre un peu après avoir bougé ces 10 pas. There’s a **Control** block that will help you here:

```blocks3
    wait (1) secs
```

\--- task \--- Add the `wait`{:class="block3control"} block into your code inside the `forever`{:class="block3control"} block, and change the number to `0.5`, like this:

```blocks3
    when green flag clicked
    forever
        move (10) steps
+      wait (0.5) secs
    end
```

\--- /task \---

## \--- collapse \---

## title: Making adjustments

The number you set in the `wait`{:class="block3control"} block says how many **seconds** you want the fish to wait. `0.5` is half a second.

You can test out different values to see which is the best for the game. And remember that you can change the number of steps inside the `move`{:class="block3motion"} block too!

\--- /collapse \---

The fish moves now, but you need it to bounce off the edge of the Stage too. Yet again, there’s a **Motion** block for this!

\--- task \--- Find the `if on edge bounce`{:class="block3motion"} block, and add it in after the `wait`{:class="block3control"} block. \--- /task \---

## \--- collapse \---

## title: What does the new block do?

The `if on edge bounce`{:class="block3motion"} block checks if the sprite is touching the edge of the Stage and, if it is, it turns left, right, up, or down as appropriate.

\--- /collapse \---

Of course, this will lead to an upside-down fish, so you need a `set rotation style`{:class="block3motion"} block again.

\--- task \--- Update your code to set the rotation style of the fish to `left-right`{:class="block3motion"} at the beginning of the sprite's script:

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

\--- task \--- Add a turn into the fish's swimming instructions, and click the green flag.

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

\--- task \--- Find the `pick random`{:class="block3operators"} **operator** block, and plug it into the `turn degrees`{:class="block3motion"} **Motion** block by clicking it and dragging it into the field where you set the number of degrees.

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

\--- task \--- Click the green flag to run the code! \--- /task \---

## \--- collapse \---

## title: So what does the forever block do now?

The forever block now makes the fish sprite do four things in order:

1. Move forward
2. Turn a little bit
3. Wait briefly
4. Check whether it's at the edge of the Stage

Once the sprite has done the check, it will start at the beginning of the loop again and move, turn, wait, check, for as long as you let your Scratch program run.

\--- /collapse \---

Cool! Next up: catching that fish!