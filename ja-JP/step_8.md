## 釣り!

サメは動き、魚は泳ぎますが、相互に干渉しません。魚がサメの口の中に泳いだ場合も、何も起こりません。 それを変える時です！

まず、魚がサメに触れているかどうかを知る必要があります。 これには、「制御」ブロックと「調べる」ブロックが必要です。

--- task ---

`もし...なら`{:class="block3control"}**制御**ブロックを、魚のスプライトの`ずっと`{:class="block3control"}ループ内の、`もし端に着いたら、跳ね返る`{:class="block3motion"}ブロックの下に追加します。

「調べる」カテゴリーの「○○に触れた」ブロックを「もし　なら」ブロックの上部のスペースにドラッグし、小さな三角形をクリックしてサメのスプライトの名前を選択します。 変更していない場合は、「Sprite1」になります。

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

--- /task ---

--- collapse ---
---
title: どのように機能しますか？
---

制御の「もし　なら」ブロックには、True / False値を指定する必要があります。

「調べる」カテゴリーのブロックは、スプライトがどこにあるのか、何に触れているのかなどの情報を収集します。 このブロックを使用しています：

```blocks3
    <touching [Sprite1 v] ?>
```

以前に演算子のところで説明したように、このブロックの先のとがった端から、「もし　なら」ブロックが必要とするTrue / False値を提供することがわかります。

--- /collapse ---

もちろん、「なら」の後の部分には何も追加せずに`もし　なら`{:class="block3control"} のブロックを追加しただけです。 そのため、現時点では、スクリプトは魚のスプライトがサメのスプライトに触れているかどうかをチェックしていますが、それに反応して何か起きるわけではありません。

「隠す」ブロックを使用すると、サメ​​が食べたように、魚を消すことができます。

--- task ---

`隠す`{:class="block3looks"}ブロックを**見た目**リストから見つけ、次のように`もし...なら`{:class="block3control"}ブロック内に配置します。

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

--- /task ---

サメが魚を捕まえると、魚は永久に消えてしまいます。 それは素晴らしいことではありません。

--- task ---

魚コードの最初の部分に**見た目**の`表示する`{:class="block3looks"}ブロックを配置すれば、ゲームをリセットをすることができます。

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

--- /task ---

ゲームはだいぶ良くなりましたが、プレイヤーが1匹の魚を捕まえるたびにゲームを再起動するようにはしたくないでしょう！

--- task ---

`もし...なら`{:class="block3control"}ブロック内のコードを次のように更新します。

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

--- /task ---

--- collapse ---
---
title: ここれはどのように作動しますか？
---

ここでは賢く振る舞いましょう：魚が隠されているとき、それは止まり、動き、そして再び現れます。

たくさんの魚が出現し続けているように見えますが、1つのスプライトが動き回っています！

--- /collapse ---

それはゲームです！ しかし、まだスコアを保持したり、勝つ方法はありません。 次のカードでそれも修正できます！