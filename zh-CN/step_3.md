## 添加和删除代码块

好赞！ 您已经编写了您的第一个Scratch程序。 是时候试试用Scratch编更多代码了! Scratch 代码由像这样的**积木块**组成：

![](images/code1.png)

所有的积木块都按其功用分类别存放在 **代码块面板中**。

## \--- collapse \---

## title: 使用不同类别的代码块

点击类别名称查看该类别中的代码块。 像这里我们选择了**运动**类：

![](images/code2a.png)

在该类别下的所有代码块都显示在了右侧的列表里：

![](images/code2b.png)

You can click on the block you want, and then just drag it into the current sprite panel and let go. 在面板中还可以移动代码块并将它们连接到一起。

\--- /collapse \---

如果要查看代码块的作用，可以双击它让它运行！

\--- task \---

尝试双击一些代码块来查看它们做什么。

\--- /task \---

## \--- collapse \---

## title: 运行代码

通常您想让代码在特定事件发生时自动运行。 这就是为什么许多程序都是从**事件**类的一个块开始的原因，最常见的是：

```blocks3
    when green flag clicked
```

与此方块连接的代码块将在点击**绿色旗帜**后运行。

代码块由上向下依次运行，所以这些代码块连接的顺序十分重要。 在这个例子中，角色将`说`{:class="block3looks"} `你好!`之后`播放`{:class="block3sound"}`meow`的声音。

```blocks3
    when green flag clicked
    say [Hello]
    play sound [meow v]
```

\--- /collapse \---

删除程序中不需要的代码块很容易！ 只需将它们拖回左侧的代码块面板即可。

**注意： **将代码块拖回动到面板会删除与拖动块相连的所有块，所以记得将要保留的代码块与要删除的代码块分开后再进行拖动。 如果您不小心误删了一些代码块，想再将它们放回来的话，用右键单击空白处，然后点击**撤消**来恢复。

![](images/code6.png)

\--- task \---

尝试添加，删除和取消删除一些代码块！

\--- /task \---

### 放在一起

我们学会了如何移动代码块，并且通过运行代码实现一些操作。接下来我们来试试如何让Scratch猫绕圈行走吧！

\--- task \---

首先选择猫作为要编辑的角色，然后将下面这些代码块拖动到角色编辑面板中，并将它们连接到一起。 代码块在**事件**和**运动**类列表中。

```blocks3
    when green flag clicked
    move [10] steps
```

\--- /task \---

\--- task \---

现在，单击舞台上方的绿色小旗。

![](images/code7.png)

\--- /task \---

这只猫会沿着直线行走……嗯......这和我们的想法不太一样对吧？

注意：如果您单击小绿旗太多次猫走远了，可以用鼠标将它拖动回去！

\--- task \---

把右转或左转代码块加到之前的代码下边，小猫就可以绕圈行走了。 这也在**动作**类列表中。

```blocks3
    when green flag clicked
    move [10] steps
+    turn cw (15) degrees
```

\--- /task \---

## \--- collapse \---

## title: 右转或左转是怎么回事？

每个圆有360度，这个代码块让角色转动15度。 您可以通过单击数字并输入新值来更改猫转动的度数和行走的步数。

![](images/code9.png)

\--- /collapse \---

\--- task \---

记得保存！

\--- /task \---