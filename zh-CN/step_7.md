## Remote-control fish

Ok, now it's time to make the fish swim on its own. To do this, you’re going to need a new kind of block: a **Control** block.

\--- task \---

Select your fish sprite.

把 `当绿旗被点击` {:class =“block3events”}块（**事件**类），`重复执行` {:class =“block3control”} 块（**控制**类），以及`移动10步` {:class =“block3motion”}块（**运动**类），拖到**角色面板** 中， 像这样：

```blocks3
    when green flag clicked
    forever
        move (10) steps
    end
```

\--- /task \---

## \--- collapse \---

## title: 新的代码块有什么作用？

**控制** 块使您的程序执行一定次数或在特定条件下运行。

在这种情况下，鱼在`重复执行`{:class="block3control"} 代码块组中一遍又一遍的执行相同的指令。 做完`重复执行`{:class="block3control"} 组块内的最后一件事(代码块)后，它会回到这个组块的开始把所有组块内的代码再执行一遍，循环往复。

\--- /collapse \---

\--- task \---

现在点击绿旗，看看会发生什么！

\--- /task \---

哦，小鱼径直坠落到舞台外边去了，而且它移动的速度也太快，鲨鱼根本追不上。

所以我们要先让小鱼的速度慢下来。 这其实很简单，只需要让它在移动10步以后稍微停顿一下。 用**控制**块可以实现这一操作：

```blocks3
    wait (1) secs
```

\--- task \---

将 `等待`{:class="block3control"} 代码块添加到`重复执行`{:class="block3control"} 块组中，将数字更改为`0.5`, 如：

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

在 `等待`{:class="block3control"} 块中设置的数字表示您想要鱼等多少**秒**。 `0.5`是半秒。

您可以通过测试不同的数值来判断停顿多久最合适。 And remember that you can change the number of steps inside the `move`{:class="block3motion"} block too!

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

Add a turn into the fish's swimming instructions, and click the green flag.

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

Click the green flag to run the code!

\--- /task \---

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