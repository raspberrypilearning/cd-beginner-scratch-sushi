## 捕鱼！

鲨鱼和小鱼分别游着，但它们之间没有任何互动：即使小鱼径直游进了鲨鱼嘴里也不会被鲨鱼吃掉。 该改变这个现状了！

首先，我们要知道鱼是否碰到了鲨鱼。 为此，我们需要一个**控制**块和一个**侦测**块。

\--- task \---

将`如果  那么`{:class="block3control"}块（**控制**类）添加到鱼的角色指令组中`重复执行`{:class="block3control</1>块组内的`碰到边缘就反弹`{:class="block3motion"} 块下边。

将`碰到  ？`{:class="block3sensing"} 块到`如果...那么`{:class="block3control"}中间的六边形空格里间，然后单击<0>碰到 ？</0>{:class="block3sensing"} 块中的小三角，从下拉菜单中选择鲨鱼角色对应的名称。 如果你没有做过修改，那么它的名字是是“Sprite1”。

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
+        if <touching [Sprite1 v] ?> then
    end
```

\--- /task \---

## \--- collapse \---

## title: 什么原理？

`如果  那么`{:class="block3control"} **控制** 块需要一个`是/否` 值。

**侦测**块收集信息，比如角色在哪里，什么是碰到，等等。 您正在使用这个块：

```blocks3
    <touching [Sprite1 v] ?>
```

从这个代码块的形状我们可以看出，它要给出`如果  那么`{:class="block3control"} 代码块所需要的`是/否`值。

\--- /collapse \---

当然，您刚刚只添加了一个`如果  那么`{:class="block3control"} 块，而没有告诉程序“那么”做什么。 所以现在你的程序脚本正在检查小鱼是否碰到了鲨鱼，但它没有做任何反应。

你可以通过使用`隐藏`{:class="block3looks"} 块来使鱼消失，就好像鲨鱼吃掉了它一样。

\--- task \---

找到 `隐藏`{:class="block3looks"} 块（ **外观**类列表中），并将其放入`如果  那么`{:class="block3control"} 块，就像这样：

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

\--- /task \---

现在，一旦鲨鱼捉到小鱼，小鱼就永远消失了。 这可不太妙。

\--- task \---

把`显示`{:class="block3looks"}块（**外观**类）拖到角色鱼代码的最开始，这样您就可以重置游戏了。

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

\--- /task \---

这已经很好，但玩家肯定不愿意每次捉到一只鱼后都要重启游戏！

\--- task \---

将`如果  那么`{:class="block3control"} 块里的代码像这样改进一下：

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

\--- /task \---

## \--- collapse \---

## title: 这是什么原理？

你太聪明了：当鱼隐藏起来后，它等待，然后换位置再出现。

看起来像很多鱼陆续出现，但其实只是那一只鱼在四周游动！

\--- /collapse \---

但这是个游戏！ 没有办法计分，也没有规则定输赢。 下一页就教您如何操作！