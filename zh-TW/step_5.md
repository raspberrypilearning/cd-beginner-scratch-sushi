## 四處移動

現在，您的鯊魚會繞圈移動，如果能用方向鍵控制它一定會更加有趣。 在這一頁，您將學習怎麼動手做！

\--- task \---

首先刪除所有有關鯊魚的代碼。

\--- /task \---

您可能已經猜到了，您將再次用到**事件**和**動作**積木！

\--- task \---

這次，找到這塊積木並將其拖曳到當前角色面板中：

```blocks3
    when [space v] key pressed
```

點擊`空白`旁邊的小箭頭(▼)。 您將會看到所有可以選擇的鍵盤按鍵。

\--- /task \---

您會需要四個`當鍵被按下` {:class=“block3events”}積木-分別對應四個方向鍵。

\--- task \---

為了要移動鯊魚，請將這些積木連接到**動作**積木，像是這樣：

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

**注意** ：`-10`表示“返回10步”。

\--- task \---

Now click the green flag to test out your code.

\--- /task \---

現在，您的鯊魚能前後移動了，這很酷吧，但它還不會上下移動。 另外，如果您瀏覽**動作**積木，您會看到沒有用於“上”或“下”的積木。 而是有一大堆關於**x**和**y**座標的積木-讓我們來試試看！

\--- task \---

Grab two `change y by`{:class="block3motion"} blocks, and update your code like this:

```blocks3
    when [up arrow v] key pressed
+     change y by (10)
```

```blocks3
    when [down arrow v] key pressed
+     change y by (-10)
```

\--- /task \---

Now when you press the arrows keys, the shark moves all around the stage!

## \--- collapse \---

## title: How do x- and y-coordinates work?

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