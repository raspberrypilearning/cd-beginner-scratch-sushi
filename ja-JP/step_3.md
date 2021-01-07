## コードブロックの追加と削除

すばらしいです！ 初めてのスクラッチプログラムを作成しました。 ここでもう少しスクラッチの馴染んで詳しくなっておきましょう。 スクラッチのコードは、次のように **ブロック**から 構成されています。

![](images/code1.png)

全てのブロックは **コードブロックパレット**の中にあり、用途のカテゴリに分類されています。

## \--- collapse \---

## title：さまざまなカテゴリのブロックを使う

カテゴリ名をクリックすると、そのカテゴリのブロックが表示されます。 ここでは、 **Motion** カテゴリが選択されています。

![](images/code2a.png)

クリックしたカテゴリ内のすべてのブロックがリストに表示されます。

![](images/code2b.png)

You can click on the block you want, and then just drag it into the current sprite panel and let go. パネルに配置したら、移動して他のブロックに接続できます。

\--- /collapse \---

ブロックの動作を確認したい場合は、ブロックをダブルクリックして実行します。

\--- task \---

Try double-clicking on some of the blocks to see what they do.

\--- /task \---

## \--- collapse \---

## title：コードの実行

Usually, you want your code to run automatically whenever something specific happens. This is why many of your programs will start with a block from the **Events** category, most often this one:

```blocks3
    緑色の旗がクリックされたとき
```

The code blocks connected to this block will run after the **green flag** is clicked.

Code blocks run from top to bottom, so the order in which you snap your blocks together matters. In this example, the sprite will `say`{:class="block3looks"} `Hello!` before it will `play`{:class="block3sound"} the `meow` sound.

```blocks3
    緑の旗がクリックされたとき
    言う [Hello]
    サウンドを再生する[meow v]
```

\--- /collapse \---

Removing or deleting code blocks you don’t want in your program is easy! Just drag them back into the code blocks palette.

**Be careful:** dragging them into the code blocks pallette will delete all the blocks connected to the block you drag, so make sure to separate code blocks you want to keep from those you want to remove. If you delete some code blocks by accident and want to get them back, right-click and then click on the **undo** option to get everything back.

![](images/code6.png)

\--- task \---

Try adding, deleting, and undeleting some code blocks!

\--- /task \---

### すべてを一緒に入れて

Now you know how to move code around and make things happen, it's time for you to create a program to make the Scratch Cat walk in a circle!

\--- task \---

Make sure you have the cat sprite selected in the sprite list, and then drag the following blocks into the sprite panel and connect them. You’ll find them in the **Events** and **Motion** lists.

```blocks3
    緑色の旗がクリックされたとき
    移動 [10] ステップ
```

\--- /task \---

\--- task \---

Now, click on the green flag above the Stage.

![](images/code7.png)

\--- /task \---

You should see the cat walking in a straight line...not exactly what you want, right?

Note: If you click the flag too many times and the cat walks away, you can drag it back!

\--- task \---

Snap the turn block to the end to make the cat sprite walk in a circle. It’s in the **Motion** list too.

```blocks3
    緑色の旗がクリックされたとき
    移動 [10] ステップ
+ cw（15）度を回す
```

\--- /task \---

## \--- collapse \---

## title：回転はどのように働くのか？

This block makes the sprite turn 15 degrees of the full 360 degrees that make up a circle. You can change that number, and the number of steps, by clicking on the number and typing in a new value.

![](images/code9.png)

\--- /collapse \---

\--- task \---

Now save your work!

\--- /task \---