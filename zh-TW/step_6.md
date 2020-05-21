## All the sprites

Now you have a shark that you can move around using the arrow keys. Nice! Time to add some fish for it to catch.

\--- task \---

Click the **New sprite** button, and on the screen that opens, choose a fish.

![The New sprite button](images/spritesNewFromLibrary.png)

If your fish is a bit big compared to your shark, you can use the size control to make both sprites the right size!

![Sprite size control](images/sprites2.png)

Change the number in the size control to make the spirte bigger or smaller.

\--- /task \---

太好了！ 接著，您將添加一些代碼，以使魚在沒有玩家幫助的情況下自行移動。 您的玩家將移動鯊魚並嘗試釣到魚。

## \--- collapse \---

## title: What about the backwards shark?

鯊魚向後游泳確實有點好笑。 就像您通常會轉身而不是向後走一樣，鯊魚會轉身而不是向後游泳。 幸運的是，Scratch為此提供了一個方法！

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

![Upside down shark](images/spritesUpsideDown.png)

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