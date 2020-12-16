## 遥控鱼

好的，现在该让鱼自己游泳了。 这里您需要一种新型的块：**控制**代码块。

\--- task \---

从角色中选择一条你喜欢的鱼。

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

## title: 调整

在 `等待`{:class="block3control"} 块中设置的数字表示您想要鱼等多少**秒**。 `0.5`是半秒。

您可以通过测试不同的数值来判断停顿多久最合适。 同样，您也可以更改`移动`{:class="block3motion"} 块内的数字改变小鱼每一次游动的距离！

\--- /collapse \---

小鱼现在可以游了，但我们还需要让它在碰到舞台边缘的时候可以游回来。 这次我们还要用到**运动**代码块！

\--- task \---

找到 `碰到边缘就反弹`{:class="block3motion"} 代码块，把它连接到`等待`{:class="block3control"} 块后。

\--- /task \---

## \--- collapse \---

## title: 新的代码块有什么作用？

`碰到边缘就反弹`{:class="block3motion"} 代码块用来检查角色是否接触到了舞台的边缘， 如果是的话则酌情转向上、下、左或右移动。

\--- /collapse \---

像之前一样，这又会使鱼倒着游，所以您需要再次设置一个`将旋转方式设为`{:class="block3motion"} 块。

\--- task \---

在脚本开始处设置鱼的旋转风格为 `左右翻转`{:class="block3motion"} ：

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

现鱼可以左右游动了。但只在一条线上游，对玩家来说太容易捉到了！ 您需要让鱼的游动方向变得不那么容易预测到。

您已经从之前的步骤中学会如何让角色转变方向，所以就从这里入手。

\--- task \---

在小鱼的游泳指令中添加转向说明，然后点击小绿旗。

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

好多了，但仍然显得有些生硬。 应该看上去随意一些。 幸运的是，Scratch 可以帮助您实现随意运动！ 只需一种新类型的代码块，称为**运算**块。

## \--- collapse \---

## title: 什么是运算符？

**运算符** 接受一个或多个值（如数字，文本或 `True / False` 值），并返回一个值。 代码块的形状代表了它会返回什么类型的值：椭圆形块给出数字或文本，六边形块给出`是/否`。

```blocks3
    (() + ())

    (join [hello ] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \---

查找`在  和  之间取随机数`{:class="block3motion"} （**运算** 类），然后点击它并将它拖到设置度数的字段，将其插入`右转  度`{:class="block3motion"} **运动**块内。

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

**注意**：您可以更改代码块中的最小值和最大值范围，但默认值 (`1` 和 `10`)对这个游戏来说就已经很合适了，所以也可以不用更改。

\--- task \---

点击绿旗来运行代码！

\--- /task \---

## \--- collapse \---

## title: 那么重复执行块组现在会做什么呢？

现在重复执行代码块让鱼依次执行四项操作：

1. 向前移动
2. 稍微转个角度
3. 短暂等待
4. 检查它自己是否处在舞台的边缘

只要让Scratch程序在运行中，这个角色就会依次执行移动，转动，等待，检查的操作，角色完成检查后会从循环的开头再次开始。

\--- /collapse \---

酷！ 下一步：捉到那条鱼！