## Poisson télécommandé

D'accord, il est maintenant temps de faire nager le poisson tout seul. Pour ce faire, tu auras besoin d’un nouveau type de bloc: un bloc **Contrôle**.

\--- task \---

Select your fish sprite.

Drag a `when green flag clicked`{:class="block3events"} **Event** block, a `forever`{:class="block3control"} **Control** block, and a `move 10 steps`{:class="block3motion"} **Motion** block into the **sprite panel**, like this:

```blocks3
    lorsque le drapeau vert est cliqué sur
    répéter indéfiniment
        déplacer de (10) pas
    fin
```

\--- /task \---

## \--- collapse \---

## title: que fait le nouveau bloc?

**Control** blocks make your program do things a certain number of times, or under certain conditions.

Here, the fish does whatever is inside the `forever`{:class="block3control"} block over and over again on a loop, forever. So once it has done the last thing (block) inside the `forever`{:class="block3control"} block, it starts over at the top and does everything again, and so on.

\--- /collapse \---

\--- task \---

Now click the green flag and watch what happens!

\--- /task \---

Well, that fish just crashed into the side of the Stage, and it was moving far too fast for your shark to catch.

First, you need to slow the fish down. That’s actually pretty easy, you just need it to wait for a little while after it moves those 10 steps. There’s a **Control** block that will help you here:

```blocks3
    attendre (1) secondes
```

\--- task \---

Add the `wait`{:class="block3control"} block into your code inside the `forever`{:class="block3control"} block, and change the number to `0.5`, like this:

```blocks3
    lorsque le drapeau vert est cliqué 
    répéter indéfiniment
        déplacer de (10) pas
+ attendre (0,5) secondes
    fin
```

\--- /task \---

## \--- collapse \---

## title: faire des ajustements

The number you set in the `wait`{:class="block3control"} block says how many **seconds** you want the fish to wait. `0.5` is half a second.

You can test out different values to see which is the best for the game. And remember that you can change the number of steps inside the `move`{:class="block3motion"} block too!

\--- /collapse \---

The fish moves now, but you need it to bounce off the edge of the Stage too. Yet again, there’s a **Motion** block for this!

\--- task \---

Find the `if on edge bounce`{:class="block3motion"} block, and add it in after the `wait`{:class="block3control"} block.

\--- /task \---

## \--- collapse \---

## title: que fait le nouveau bloc?

The `if on edge bounce`{:class="block3motion"} block checks if the sprite is touching the edge of the Stage and, if it is, it turns left, right, up, or down as appropriate.

\--- /collapse \---

Of course, this will lead to an upside-down fish, so you need a `set rotation style`{:class="block3motion"} block again.

\--- task \---

Update your code to set the rotation style of the fish to `left-right`{:class="block3motion"} at the beginning of the sprite's script:

```blocks3
    lorsque le drapeau vert est cliqué 
+ définir le style de rotation [gauche-droite v]
    répéter indéfiniment
        déplacer de (10) pas
        attendre (0.5) secs
        si sur le bord, rebondir
    fin
```

\--- /task \---

The fish moves backwards and forwards now, but only in a straight line — a bit too easy for the player to catch with the shark! You need to make the fish less predictable.

You already know from a previous step how to make a sprite turn, so start there.

\--- task \---

Add a turn into the fish's swimming instructions, and click the green flag.

```blocks3
    lorsque le drapeau vert est cliqué 
    définir le style de rotation [gauche-droite v]
    répéter indéfiniment
        déplacer de (10) pas
+ tourner cw (10) degrés
        attendre (0.5) secs
        si sur le bord, rebondir
    fin
```

\--- /task \---

It’s better, but there’s still too much of a pattern. It needs to be more random. Luckily, Scratch can do random for you! You’ll just need a new kind of block, called an **operator** block.

## \--- collapse \---

## title: Qu'est-ce qu'un opérateur?

**Operators** take in one or more values (like numbers, text, or `True/False` values) and give back a single value. You can tell the kind of value it will give back by the shape of the block: round ends give numbers or text, pointy ends give `True/False`.

```blocks3
    (() + ())

    (rejoindre [bonjour] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \---

Find the `pick random`{:class="block3operators"} **operator** block, and plug it into the `turn degrees`{:class="block3motion"} **Motion** block by clicking it and dragging it into the field where you set the number of degrees.

```blocks3
    lorsque le drapeau vert est cliqué
    définir le style de rotation [gauche-droite v]
    répéter indéfiniment
        déplacer de (10) pas
+ tourner cw (choisir au hasard (1) à (10)) degrés
        attendre (0.5) secondes
        si sur le bord, rebondir
    fin
```

\--- /task \---

**Note**: you can change the minimum and maximum numbers it will pick, but the default values (`1` and `10`) are pretty good for this game, so you can just leave them.

\--- task \---

Click the green flag to run the code!

\--- /task \---

## \--- collapse \---

## title: Alors, que fait maintenant le bloc répéter indéfiniment ?

The forever block now makes the fish sprite do four things in order:

1. Avancer
2. Tourner un peu
3. Attendre brièvement
4. Vérifier si c'est au bord de la scène

Once the sprite has done the check, it will start at the beginning of the loop again and move, turn, wait, check, for as long as you let your Scratch program run.

\--- /collapse \---

Cool! Next up: catching that fish!