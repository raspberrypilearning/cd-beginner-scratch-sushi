## 釣り!

サメは動き、魚は泳ぎますが、相互に干渉しません。魚がサメの口の中に泳いだ場合も、何も起こりません。 それを変える時です！

まず、魚がサメに触れているかどうかを知る必要があります。 これには、「制御」ブロックと「調べる」ブロックが必要です。

\--- task \---

Add the `if...then`{:class="block3control"} **Control** block inside the `forever`{:class="block3control"} loop of the fish sprite, below the `if on edge bounce`{:class="block3motion"} block.

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

\--- /task \---

## \--- collapse \---

## タイトル: どのように機能しますか？

制御の「もし　なら」ブロックには、True / False値を指定する必要があります。

「調べる」カテゴリーのブロックは、スプライトがどこにあるのか、何に触れているのかなどの情報を収集します。 このブロックを使用しています：

```blocks3
    <touching [Sprite1 v] ?>
```

以前に演算子のところで説明したように、このブロックの先のとがった端から、「もし　なら」ブロックが必要とするTrue / False値を提供することがわかります。

\--- /collapse \---

Of course, you’ve just added an `if...then`{:class="block3control"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

「隠す」ブロックを使用すると、サメ​​が食べたように、魚を消すことができます。

\--- task \---

Find the `hide`{:class="block3looks"} block in the **Looks** list, and put it inside the `if...then`{:class="block3control"} block, like so:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

\--- /task \---

サメが魚を捕まえると、魚は永久に消えてしまいます。 それは素晴らしいことではありません。

\--- task \---

Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \---

Update the code inside your `if...then`{:class="block3control"} block to look like this:

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

## title: How does this work?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!