## Adding and removing code blocks

太好了！ 您已經編寫了第一個Scratch程序。 是時候學習更多有關編寫Scratch代碼的知識了！ Scratch代碼是由**積木**組成的，例如：

![](images/code1.png)

您會在**代碼積木面板**中找到所有的積木 ，根據他們的工作分為不同的類別。

## \--- collapse \---

## 標題：使用來自不同類別的積木

點擊類別名稱以查看該類別中的積木。 這裡選擇了**動作**類別：

![](images/code2a.png)

All of the blocks in the category you've clicked are shown in a list:

![](images/code2b.png)

You can click on the blcok you want, and then just drag it into the current sprite panel and let go. Once it's in the panel, you can move it around and connect it to other blocks.

\--- /collapse \---

If you want to see what a block does, you can double-click on it to make it run!

\--- task \---

Try double-clicking on some of the blocks to see what they do.

\--- /task \---

## \--- collapse \---

## title: Running the code

Usually, you want your code to run automatically whenever something specific happens. This is why many of your programs will start with a block from the **Events** category, most often this one:

```blocks3
    when green flag clicked
```

The code blocks connected to this block will run after the **green flag** is clicked.

Code blocks run from top to bottom, so the order in which you snap your blocks together matters. In this example, the sprite will `say`{:class="block3looks"} `Hello!` before it will `play`{:class="block3sound"} the `meow` sound.

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