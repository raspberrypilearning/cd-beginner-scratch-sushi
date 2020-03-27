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

そのサメが後ろに泳いでいるのは少しおかしく見えます。 Just like you’d usually turn around rather than walking backwards, the shark would turn around rather than swimming backwards. Luckily for you, Scratch has a block for this!

The `point in direction`{:class="block3motion"} block lets you pick the direction your sprite is pointing in. You’ll find it in the **Motion** blocks section. You can type in any number of degrees, to point the sprite wherever you want.

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

If you try moving the shark around now after you've added the `point in direction`{:class="block3motion"} blocks, you might notice something a little strange happening. The shark may not be turning quite right!

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