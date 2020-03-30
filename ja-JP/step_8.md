## 釣り!

サメは動き、魚は泳ぎますが、相互に干渉しません。魚がサメの口の中に泳いだ場合も、何も起こりません。 それを変える時です！

まず、魚がサメに触れているかどうかを知る必要があります。 これには、「制御」ブロックと「調べる」ブロックが必要です。

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

「調べる」カテゴリーの「○○に触れた」ブロックを「もし　なら」ブロックの上部のスペースにドラッグし、小さな三角形をクリックしてサメのスプライトの名前を選択します。 変更していない場合は、「Sprite1」になります。

```blocks3
    緑の旗が押されたとき
+回転方法を左右のみにする
    ずっと
        （10）歩動かす
+　　　1から10までの乱数　度回す　
        （0.5）秒待つ
        もし端に着いたら、跳ね返る
+　　　もし　なら
    終了
```

\--- /task \---

## \--- 折りたたむ \---

## タイトル: どのように機能しますか？

制御の「もし　なら」ブロックには、True / False値を指定する必要があります。

「調べる」カテゴリーのブロックは、スプライトがどこにあるのか、何に触れているのかなどの情報を収集します。 このブロックを使用しています：

```blocks3
    Sprite1に触れた
```

以前に演算子のところで説明したように、このブロックの先のとがった端から、「もし　なら」ブロックが必要とするTrue / False値を提供することがわかります。

\--- /collapse \---

もちろん、「なら」の後の部分には何も追加せずに`もし　なら`{:class="block3control"} のブロックを追加しただけです。 そのため、現時点では、スクリプトは魚のスプライトがサメのスプライトに触れているかどうかをチェックしていますが、それに反応して何か起きるわけではありません。

「隠す」ブロックを使用すると、サメ​​が食べたように、魚を消すことができます。

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    もし　Sprite1に触れた　なら
+　隠す
終了
```

\--- /task \---

サメが魚を捕まえると、魚は永久に消えてしまいます。 それは素晴らしいことではありません。

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    緑の旗が押されたとき
+　表示する
　回転方法を[左右のみ]にする
    ずっと
```

\--- /タスク \---

ゲームはだいぶ良くなりましたが、プレイヤーが1匹の魚を捕まえるたびにゲームを再起動するようにはしたくないでしょう！

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    もし端に着いたら、跳ね返る
　もし　なら
        隠す
+　　（1）秒待つ
+ 1秒でx座標を：（（-240）から（240）までの乱数に）y座標を：（（-180）から（180までの乱数に） ））に変える
+　  表示する
    終了
```

\--- /task \---

## \--- 折りたたむ \---

## タイトル：ここれはどのように作動しますか？

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

たくさんの魚が出現し続けているように見えますが、1つのスプライトが動き回っています！

\--- /collapse \---

それはゲームです！ しかし、まだスコアを保持したり、勝つ方法はありません。 次のカードでそれも修正できます！