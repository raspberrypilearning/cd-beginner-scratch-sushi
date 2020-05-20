## Adding and removing code blocks

太好了！ 您已經編寫了第一個Scratch程序。 是時候學習更多有關編寫Scratch代碼的知識了！ Scratch代碼是由**積木**組成的，例如：

![](images/code1.png)

您會在**代碼積木面板**中找到所有的積木 ，根據他們的工作分為不同的類別。

## \--- collapse \---

## 標題：使用來自不同類別的積木

點擊類別名稱以查看該類別中的積木。 這裡選擇了**動作**類別：

![](images/code2a.png)

在您點擊類別後將顯示該類別中所有的積木：

![](images/code2b.png)

您可以點擊您想要的積木並將其拖曳到當前角色面板中並放開。 一旦積木在面板中，就可以移動它並與其他積木相連接。

\--- /collapse \---

如果要查看積木的功能，您可以雙擊它來運行！

\--- task \---

嘗試雙擊某些積木來查看它們的功能。

\--- /task \---

## \--- collapse \---

## 標題：運行代碼

通常，您會希望代碼在特定情況下自動運行。 這就是為什麼許多程序都是從**事件**類別裡的積木當起頭的原因，最常見的是：

```blocks3
    when green flag clicked
```

連接到這塊積木後面的積木將會在按下**綠色旗標**之後運行。

代碼積木是從上到下運行的，因此將代碼積木組合在一起的順序很重要。 In this example, the sprite will `say`{:class="block3looks"} `Hello!` before it will `play`{:class="block3sound"} the `meow` sound.

```blocks3
    when green flag clicked
    say [Hello]
    play sound [meow v]
```

\--- /collapse \---

Removing or deleting code blocks you don’t want in your program is easy! Just drag them back into the code blocks palette.

**Be careful:** dragging them into the code blocks pallette will delete all the blocks connected to the block you drag, so make sure to separate code blocks you want to keep from those you want to remove. If you delete some code blocks by accident and want to get them back, right-click and then click on the **undo** option to get everything back.

![](images/code6.png)

\--- task \---

Try adding, deleting, and undeleting some code blocks!

\--- /task \---

### Putting it all together

Now you know how to move code around and make things happen, it's time for you to create a program to make the Scratch Cat walk in a circle!

\--- task \---

Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. You’ll find them in the **Events** and **Motion** lists.

```blocks3
    when green flag clicked
    move [10] steps
```

\--- /task \---

\--- task \---

Now, click on the green flag above the Stage.

![](images/code7.png)

\--- /task \---

You should see the cat walking in a straight line...not exactly what you want, right?

Note: If you click the flag too many times and the cat walks away, you can drag it back!

\--- task \---

Snap the turn block to the end to make the cat sprite walk in a circle. It’s in the **Motion** list too.

```blocks3
    when green flag clicked
    move [10] steps
+    turn cw (15) degrees
```

\--- /task \---

## \--- collapse \---

## title: How does turning work?

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. You can change that number, and the number of steps, by clicking on the number and typing in a new value.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Now save your work!

\--- /task \---