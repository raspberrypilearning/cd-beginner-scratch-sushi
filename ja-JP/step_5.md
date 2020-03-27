## 物を動かす

今、あなたのサメは円を描いて動きます。矢印キーでそれを制御する方がずっと楽しいでしょう。 このカードでは、その方法を学習します！

\--- task \---

Start by deleting all code that you have for the shark.

\--- /task \---

おそらくご想像のとおり、再び「イベント」ブロックと「動き」ブロックが必要になります！

\--- task \---

This time, look for this block and drag it into the current sprite panel:

```blocks3
    when [space v] key pressed
```

スペースの横にある小さな下矢印（▼）をクリックします 。 選択できるすべてのキーボードキーのリストが表示されます。

\--- /task \---

キーが押されたときのブロックが4つ必要になります（矢印キーごとに1つ）。

\--- task \---

To make your shark move, connect these blocks to **Motion** blocks like this:

```blocks3
    when [left arrow v] key pressed
    move (-10) steps
```

```blocks3
    when [right arrow v] key pressed
    move (10) steps
```

```blocks3
    when [up arrow v] key pressed
```

```blocks3
    when [down arrow v] key pressed
```

\--- /task \---

注：-10は「10ステップ戻る」ことを意味します。

\--- task \---

Now click the green flag to test out your code.

\--- /task \---

これでサメが前後に移動します。これはかなりクールですが、上下には移動しません。 また、「動き」ブロックを見ると、「上」または「下」のブロックがないことがわかります。 ただし、x座標とy座標に関連するものはたくさんあります。それらを試してみましょう。

\--- task \---

Grab two `change y by`{:class="block3motion"} blocks, and update your code like this:

```blocks3
    when [up arrow v] key pressed
+     change y by (10)
```

```blocks3
    when [down arrow v] key pressed
+     change y by (-10)
```

\--- /task \---

矢印キーを押すと、サメがステージ全体を動き回ります！

## \--- collapse \---

## タイトル：x座標とy座標はどのように機能しますか？

スプライトなどのオブジェクトの位置について話すために、x座標とy座標をよく使用します。 ステージ座標のx軸は左から右に伸び、y軸は下から上に伸びています。

![](images/moving3.png)

A sprite can be located by the coordinates of its centre, for example `(15, -27)`, where `15` is its position along the x-axis , and `-27` its position along the y-axis.

+ これが実際にどのように機能するかを理解するには、スプライトを選択し、xおよびyコントロールを使用して、座標に異なる値を設定してステージ上でスプライトを移動します。

![](images/xycoords.png)

+ 異なる値のペアを試して、スプライトがどこに行くかを確認してください！ スクラッチでは、x軸は-240から240になり、y軸は-180から180になります。

\--- /collapse \---

### ゲームを再起動する

サメは画面全体を移動しますが、これがゲームだと想像してください。どのように再起動し、各ゲームの開始時に何が起こるのでしょうか？

プレイヤーがゲームを開始するときに、サメを元の場所に戻す必要があります。 They'll start this game by clicking on the green flag, so you need to change the shark sprite's x- and y-coordinates when that happens.

That’s actually pretty easy! ステージの中心は、（x、y）座標の（0、0）です。

したがって、必要なのは、その緑色の旗のイベントブロックと、「動き」にある「x座標を○、y座標を○にする」ブロックです。

\--- task \---

Drag a `when green flag clicked`{:class="block3events"} **Event** block onto the current sprite panel.

```blocks3
    when green flag clicked
```

次に、「動き」にある「x座標を○、y座標を○にする」ブロックを見つけて、緑の旗イベントブロックに添付します。

```blocks3
    when green flag clicked
+     go to x: (0) y: (0)
```

Set the both the `x` and the `y` coordinate to `0` in the `go to`{:class="block3motion"} block if they are not already `0`.

\--- /task \---

\--- task \---

Now click the green flag: you should see the shark return to the centre of the stage!

\--- /task \---