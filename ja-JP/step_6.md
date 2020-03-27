## すべてのスプライト

これで、矢印キーを使用して移動できるサメができました。 すばらしい！ 魚を追加して捕まえる時間です。

\--- task \---

[ 新規スプライト ]ボタンをクリックし、開いた画面で魚を選択します。

![新しいスプライトボタン](images/spritesNewFromLibrary.png)

サメに比べて魚が少し大きい場合は、サイズコントロールを使用して両方のスプライトを適切なサイズにすることができます！

![スプライトのサイズを調整](images/sprites2.png)

サイズコントロールの数値を変更して、追加した魚のスプライトを大きくまたは小さくします。

\--- /task \---

素晴らしいです！ 後で、プレイヤーの助けを借りずに、魚を自力で動き回らせるためのコードを追加します。 プレイヤーはサメを動かし、魚を捕まえようとします。

## \--- collapse \---

## タイトル：後方のサメはどうですか？

そのサメが後ろに泳いでいるのは少しおかしく見えます。 後方を泳ぐのではなく通常は向きを変えるように、サメは向きを変えます。 幸いなことに、Scratchにはこのためのブロックがあります！

「○度に向ける」ブロックを使用すると、スプライトが指している方向を選択できます。 これは[動き]セクションにあります。 任意の角度で入力して、好きな場所にスプライトを向けることができます。

\--- /collapse \---

\--- task \---

Grab a couple of copies of the `point in direction`{:class="block3motion"} block from the **Motion** list and connect them to your shark's code, like this:

```blocks3
    when [left arrow v] key pressed
+     point in direction (-90)
    move (10) steps
```

```blocks3
    when [right arrow v] key pressed
+     point in direction (90)
    move (10) steps
```

\--- /task \---

\--- task \---

Change the number of steps in the `move`{:class="block3motion"} blocks from `-10` to `10`.

方向ブロックにポイントを追加した後、サメを今すぐ動かしてみると、少し奇妙なことが起こっていることに気付くかもしれません。 サメは完全に右に曲がっていないかもしれません！

![Upside down shark](images/spritesUpsideDown.png)

\--- /task \---

## \--- collapse \---

## title: Why does it go upside down?

The problem here is that the shark sprite started, as all sprites do, with the 'all around' **rotation style**, and what you need it to have is the 'left-right' style.

As usual, there’s a block for that, and it’s in **Motion**!

\--- /collapse \---

\--- task \---

Look in the **Motion** category for the block `set rotation style`{:class="block3motion"}.

Add the block to your shark reset code from earlier, and set the rotation style to `left-right`{:class="block3motion"}, like this:

```blocks3
    when green flag clicked
+     set rotation style [left-right v]
    go to x: (0) y: (0)
```

\--- /task \---