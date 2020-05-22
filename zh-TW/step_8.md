## 釣魚！

鯊魚移動了，魚游泳了，但是卻沒有相互作用：如果魚游到鯊魚的嘴裡，什麼也不會發生。 是時候改變了！

首先，您需要知道魚是否碰到鯊魚。 為此，您需要一個**控制**積木和**偵測**積木。

\--- task \---

在魚的`重複無限次`{:class=“block3control”}迴圈內，`碰到邊緣就反彈`{:class=“block3motion”}積木的下面添加`如果...那麼`{:class=“block3control”}**控制**積木。

拖曳`碰到... `{:class=“block3sensing”}積木到`如果...那麼`{:class=“block3control”}積木上面的空格處，然後點擊小三角形並選擇鯊魚的名稱。 如果您還沒改過名稱，則為“ 角色1”。

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

## 標題：它是怎麼運作的？

`如果...那麼`{:class=“block3control”}**控制**積木需要給它`對/錯`的值。

**偵測**積木會收集資訊，例如角色的位置、它碰到什麼之類的。 您正在使用以下代碼積木：

```blocks3
    <touching [Sprite1 v] ?>
```

由於這塊積木是有角的，您可以知道它會給您`對/錯`的值，`如果...那麼`{:class=“block3control"}積木也需要這樣的值。

\--- /collapse \---

當然，您剛剛添加了`如果...那麼`{:class=“block3control”}積木，但是還沒在'那麼'部分添加任何東西。 所以現在您的腳本只會檢查魚是否碰到鯊魚，但還沒有為此做出任何反應。

您可以在鯊魚吃了它之後，使用`隱藏`{:class=“block3looks”}積木讓魚變不見。

\--- task \---

在**外觀**清單中找到`隱藏`{:class=“block3looks”}積木，然後將它放在`如果...那麼`{:class=“block3control”}積木內，如下所示：

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

\--- /task \---

現在一旦鯊魚抓捕到魚，魚就會永遠消失了。 這樣不是很好。

\--- task \---

把**外觀**裡的`顯示`{:class=“block3looks”}積木放到代碼的最前面，這樣您才可以重置遊戲。

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

\--- /task \---

現在已經很好了，但是您應該不希望玩家在每次釣到魚的時候都會重新遊戲吧！

\--- task \---

調整一下`如果...那麼`{:class=“block3control”}積木裡面的代碼，看起來像這樣：

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

## 標題：它是如何運作的？

現在變得更靈活了：當魚被隱藏的時候，它會等待、移動然後再次出現。

這樣看起來好像有很多魚在不斷地出現，但是那是同一隻魚在四處移動！

\--- /collapse \---

這是一場遊戲！ 但是還沒有紀錄分數或獲勝的方式。 您也可以解決此問題-在下一頁！