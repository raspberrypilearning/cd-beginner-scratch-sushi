## 让角色四处移动

您的鲨鱼现在可以围成一圈移动，如果能用箭头键控制它的话会更加有趣。 这一步就教您如何做到！

\--- task \---

首先删除所有有关鲨鱼的代码。

\--- /task \---

您可能已经猜到了，您又需要用到**事件**和**运动**代码块了！

\--- task \---

这次，查找此块并将其拖动到当前角色的面板中：

```blocks3
    when [space v] key pressed
```

点击`空格`旁边的小箭头(▼)。 会出现一个包含所有按键的下拉菜单可供选择。

\--- /task \---

您一共需要4个`当按下   键`{:class="block3events"} 代码块——给每个方向箭头使用一个。

\--- task \---

想要让鲨鱼移动，需要将这些代码块像这样连接到**运动**代码块上：

```blocks3
    when [left arrow v] key pressed
    move (-10) steps
```

```blocks3
    when [right arrow v] key pressed
    move (10) steps
```

```blocks3
    when [up arrow v] key pressed
```

```blocks3
    when [down arrow v] key pressed
```

\--- /task \---

**注意**：`-10`表示“后退10步”。

\--- task \---

单击绿色小旗标志来测试您的代码。

\--- /task \---

现在鲨鱼可以前后移动了，但还不能上下移动。 而且，**运动**代码块中也并没有用于“上”或“下”的块。 但我们有一整套关于**x**和**y**坐标的操作——让我们试试吧！

\--- task \---

拖两个`将y坐标设为 `{:class="block3motion"} 的代码块，并按如下所示更新您的代码：

```blocks3
    when [up arrow v] key pressed
+     change y by (10)
```

```blocks3
    when [down arrow v] key pressed
+     change y by (-10)
```

\--- /task \---

现在当您再按方向键时，鲨鱼就可以在这个舞台上四处移动了！

## \--- collapse \---

## title: x和y坐标的工作原理是什么？

To talk about the positions of objects, such as sprites, we often use x- and y-coordinates. The **x-axis** of the Stage coordinate system runs from **left to right**, and the **y-axis** runs from **bottom to top**.

![](images/moving3.png)

A sprite can be located by the coordinates of its centre, for example `(15, -27)`, where `15` is its position along the x-axis , and `-27` its position along the y-axis.

+ To get a feel for how this actually works, select a sprite and use the **x** and **y** controls to move it around the stage by setting different values for the coordinates.

![](images/xycoords.png)

+ Try different pairs of values to see where the sprite goes! In Scratch, the x-axis goes from `-240` to `240`, and the y-axis goes from `-180` to `180`.

\--- /collapse \---

### Restarting the game

The shark moves all over the screen now, but imagine this is a game: how do you restart it, and what happens at the start of each game?

You need to get the shark to its original location when the player starts the game. They'll start this game by clicking on the green flag, so you need to change the shark sprite's x- and y-coordinates when that happens.

That’s actually pretty easy! The centre of the stage is `(0, 0)` in `(x, y)` coordinates.

So all you need is an **Event** block for that green flag, and the **go to** block from **Motion**.

\--- task \---

Drag a `when green flag clicked`{:class="block3events"} **Event** block onto the current sprite panel.

```blocks3
    when green flag clicked
```

Then find the `go to`{:class="block3motion"} **Motion** block, and attach it to your flag **Event** block.

```blocks3
    when green flag clicked
+     go to x: (0) y: (0)
```

Set the both the `x` and the `y` coordinate to `0` in the `go to`{:class="block3motion"} block if they are not already `0`.

\--- /task \---

\--- task \---

Now click the green flag: you should see the shark return to the centre of the stage!

\--- /task \---