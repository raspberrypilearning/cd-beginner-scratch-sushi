## 自力で動く魚

さて、今度は魚を自力で泳がせます。 これを行うには、新しい種類のブロックが必要になります：「制御」カテゴリーのブロック。

\--- task \---

Select your fish sprite.

Drag a `when green flag clicked`{:class="block3events"} **Event** block, a `forever`{:class="block3control"} **Control** block, and a `move 10 steps`{:class="block3motion"} **Motion** block into the **sprite panel**, like this:

```blocks3
    緑の旗が押されたとき
　ずっと
       (10）歩動かす
    終了
```

\--- /task \---

## \--- 折りたたむ \---

## タイトル：新しいブロックは何をしますか？

制御ブロックは、プログラムに特定の回数、または特定の条件下で物事をさせます。

ここで、魚は「ずっと」のブロック内にあるものは何でも、ループ(繰り返し)で何度も繰り返し実行します。 したがって、「ずっと」ブロック内で最後の処理（ブロック）が完了すると、最初からやり直して、すべてを繰り返します。

\--- /collapse \---

\--- task \---

Now click the green flag and watch what happens!

\--- /task \---

Well, that fish just crashed into the side of the Stage, and it was moving far too fast for your shark to catch.

まず、魚を遅くする必要があります。 That’s actually pretty easy, you just need it to wait for a little while after it moves those 10 steps. ここで役立つ制御ブロックがあります。

```blocks3
    1 秒待つ
```

\--- task \---

Add the `wait`{:class="block3control"} block into your code inside the `forever`{:class="block3control"} block, and change the number to `0.5`, like this:

```blocks3
    緑の旗が押されたとき
    ずっと
        （10）歩動かす
+（0.5）秒待つ
    終了
```

\--- /task \---

## \--- 折りたたむ \---

## タイトル：調整する

待機ブロックに設定した数値は、魚を何秒間待機させたいかを示しています。 0.5は0.5秒です。

さまざまな値をテストして、ゲームに最適な値を確認できます。 また、移動ブロック内の歩数も変更できることを忘れないでください！

\--- /折りたたむ \---

The fish moves now, but you need it to bounce off the edge of the Stage too. 繰り返しになりますが、これには「動き」ブロックがあります！

\--- task \---

Find the `if on edge bounce`{:class="block3motion"} block, and add it in after the `wait`{:class="block3control"} block.

\--- /task \---

## \--- 折りたたむ \---

## タイトル：新しいブロックは何をしますか？

The `if on edge bounce`{:class="block3motion"} block checks if the sprite is touching the edge of the Stage and, if it is, it turns left, right, up, or down as appropriate.

\--- /collapse \---

もちろん、これは逆さまの魚につながるため、再び回転方法の設定が必要になります。

\--- task \---

Update your code to set the rotation style of the fish to `left-right`{:class="block3motion"} at the beginning of the sprite's script:

```blocks3
    緑のフラグが押されたとき
+回転方法を左右のみにする
    ずっと
        （10）歩動かす
        （0.5）秒待つ
        もし端に着いたら、跳ね返る
    終了
```

\--- /task \---

魚は今では前後に動きますが、直線でしかありません。プレイヤーがサメを捕まえるのは少し簡単すぎます！ 魚の動きを予測しにくくする必要があります。

前のステップでスプライトを回転させる方法をすでに知っているので、そこから始めます。

\--- task \---

Add a turn into the fish's swimming instructions, and click the green flag.

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

それは良いですが、まだパターンが多すぎます。 よりランダムにする必要があります。 幸いなことに、Scratchはあなたのためにランダムにできます！ You’ll just need a new kind of block, called an **operator** block.

## \--- collapse \---

## タイトル：演算子とは何ですか？

演算子は、1つ以上の値（数値、テキスト、True / False値など）を受け取り、単一の値を返します。 ブロックの形状によって返される値の種類を知ることができます。丸い端は数字またはテキストを与え、尖った端は True / Falseを与えます 。

```blocks3
    (() + ())

    (join [hello ] [world])

    <[] = []>
```

\--- /collapse \---

\--- task \---

Find the `pick random`{:class="block3operators"} **operator** block, and plug it into the `turn degrees`{:class="block3motion"} **Motion** block by clicking it and dragging it into the field where you set the number of degrees.

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

注：乱数の選択する最小数と最大数は変更できますが、このゲームではデフォルト値（1と10）で十分なので、そのままにしておくことができます。

\--- task \---

Click the green flag to run the code!

\--- /task \---

## \--- collapse \---

## タイトル：では、「ずっと」ブロックは今何をしていますか？

「ずっと」ブロックは、魚のスプライトに4つのことを順番に実行させるようになりました。

1. 前進する
2. 少し回します
3. ちょっと待つ
4. ステージの端にあるかどうかを確認します

スプライトがチェックを完了すると、スクラッチプログラムを実行する限り、ループの先頭から再び開始し、移動、回転、待機、チェックを行います。

\--- /collapse \---

素敵! 次はその魚を捕まえましょう！