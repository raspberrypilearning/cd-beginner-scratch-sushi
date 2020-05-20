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

代碼積木是從上到下運行的，因此將代碼積木組合在一起的順序很重要。 在這個範例中，角色會在`播放`{:class=“block3sound”}`meow`音效之前`說出`{:class=“block3looks”}`Hello!`。

```blocks3
    when green flag clicked
    say [Hello]
    play sound [meow v]
```

\--- /collapse \---

在您的程序中移除或刪除你不需要的代碼積木是很容易的！ 只需將它們拖曳回代碼積木面板就可以了。

**注意：**將不需要的積木拖回代碼積木面板會將所有跟它相連的積木一起刪除，所以請確保將要保留的代碼塊與要刪除的代碼塊分開。 如果您不小心刪除了一些代碼積木並想復原，請點擊右鍵，然後點擊**復原**選項讓一切恢復原。

![](images/code6.png)

\--- task \---

嘗試添加，刪除和取消刪除一些代碼積木！

\--- /task \---

### 把它們結合

現在您知道如何移動並運行代碼了，現在是時候創建一個程序來使Scratch 貓走一圈了！

\--- task \---

確保在“角色”列表中選擇了貓角色，然後將下面這塊積木拖曳到“角色”面板中並進行連接。 您可以在**事件**以及**動作**列表中找到它們。

```blocks3
    when green flag clicked
    move [10] steps
```

\--- /task \---

\--- task \---

現在，單擊舞台上方的綠色旗標。

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