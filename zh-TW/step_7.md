## 遙控魚

好的，現在是時候讓魚自行游泳了。 為此，您將需要一種新的積木：**控制**積木。

\--- task \---

選擇您要的魚。

拖曳一個`當綠色旗標被點擊`{:class=“block3events”} **事件**積木、一個`重複無限次` {:class=“block3control”}**控制**積木，還有一個`移動10點`{:class=“block3motion”}**動作**積木到**角色面板**中，像這樣：

```blocks3
    when green flag clicked
    forever
        move (10) steps
    end
```

\--- /task \---

## \--- collapse \---

## title：新的積木有什麼功能？

**控制**積木使您的程序能執行特定次數或在特定條件下運行。

在這裡，魚在`重複無限次`{:class=“block3control”}積木內一次又一次地一直重複做一樣的事情。 所以在`重複無限次` {:class=“block3control”}積木內，一旦完成最後一件事(積木)，它就會從頂部再重新執行一次，依此類推。

\--- /collapse \---

\--- task \---

現在點擊綠色的旗子，看看會發生什麼事。

\--- /task \---

好吧，那條魚剛剛直接衝向舞台的邊邊了，並且移動得太快了，鯊魚很難捉到。

首先，您需要放慢速度。 這實際上很容易，只要在移動這10步後，等待一會兒即可。 這裡有一個能幫助到您的**控制**積木：

```blocks3
    wait (1) secs
```

\--- task \---

添加`等待` {:class=“block3control”}積木到`重複無限次`{:class=“block3control”}積木中，並將數字更改為`0.5`，像這樣：

```blocks3
    when green flag clicked
    forever
        move (10) steps
+      wait (0.5) secs
    end
```

\--- /task \---

## \--- collapse \---

## 標題：進行調整

您在`等待` {:class=“block3control”}積木中設置的數字，表示你想讓魚等待多少**秒**。 `0.5`表示一秒的一半。

您可以測試不同的值，看看哪個最適合遊戲。 請記住，您也可以更改`移動`{:class=“block3motion”}積木中的步數！

\--- /collapse \---

魚現在可以移動了，但是您也需要讓它有碰到舞台邊緣就反彈的功能。 再一次，**動作**類別中有針對這個的積木！

\--- task \---

請找到`碰到邊緣就反彈`{:class=“block3motion”}積木，並把它加在`等待`{:class=“block3control”}積木後面。

\--- /task \---

## \--- collapse \---

## title：新的積木有什麼功能？

`碰到邊緣就反彈`{:class=“block3motion”}積木會檢查角色是否接觸到舞台的邊緣，如果是，則會適當地向左，向右，向上或向下旋轉。

\--- /collapse \---

當然，這可能導致出現顛倒的魚，因此您需要再次使用`迴轉方式設為` {:class=“block3motion”}積木。

\--- task \---

更新您的代碼，在角色腳本的開頭將魚的迴轉方式設置為`左-右` {:class=“block3motion”}：

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

魚現在可以前後移動了，但只能直線移動-對於玩家來說太容易了！ 所以您需要讓魚更難預測它的路徑。

您已經從上一步知道如何讓角色轉彎，所以從這裡開始。

\--- task \---

在魚的游泳代碼中添加一個轉彎，然後點擊綠色旗標。

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

這樣比較好了，但還是有太固定的模式了。 它需要變得更隨機一點。 幸運的是，Scratch可以為您做到隨機的功能！ 您只需要一種新的積木，稱為**運算**積木。

## \--- collapse \---

## 標題：什麼是運算符號？

**運算符號**接受一個或多個值（例如數字，文本或`對/錯`值）並返回一個值。 您可以透過積木的形狀判斷返回的值的類型：圓形的是數字或文本，有角的是`真/假` 。

```blocks3
    (() + ())

    (join [hello ] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \---

找到`隨機取數`{:class=“block3operators”}**運算符號**積木，然後點擊並拖曳到`旋轉` {:class=“block3motion”}**動作**積木中設定度數的地方。

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

**注意**：您可以更改它能選擇的最小值和最大值，但默認值（`1`和`10`）對於這個遊戲來說非常適合，因此您可以不用動它。

\--- task \---

點擊綠色旗標來運行代碼！

\--- /task \---

## \--- collapse \---

## 標題：那麼重複無限次的積木現在會做什麼？

現在重複無限次積木使魚按照順序執行四項操作：

1. 前進
2. 旋轉一點
3. 稍微等待一下
4. 檢查它是否在舞台的邊緣

一旦角色完成檢查，只要您的Scratch程序持續運行，它就會在迴圈的開頭再次開始並移動、轉動、等待、檢查持續下去。

\--- /collapse \---

很酷！ 下一步：釣到那條魚！