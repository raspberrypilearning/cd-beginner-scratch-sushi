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

目的のブロックをクリックして、現在のスプライトパネルにドラッグして放します。 パネルに配置したら、移動して他のブロックに接続できます。

\--- /collapse \---

ブロックの動作を確認したい場合は、ブロックをダブルクリックして実行します。

\--- task \---

一部のブロックをダブルクリックしてみて、それらの機能を確認してください。

\--- /task \---

## \--- collapse \---

## title：コードの実行

通常、何か特定の事象が発生したときにコードが自動的に実行されるようにしたいです。 これが、多くのプログラムが**イベント**カテゴリーのブロックから始まる理由です。最も多いのはこれです。

```blocks3
    緑色の旗がクリックされたとき
```

このブロックに接続されたコードブロックは、**緑色のフラグ**がクリックされた後に実行されます。

コードブロックは上から下へと動くので、ブロックをくっつける順番が重要です。 この例では、スプライトは`ニャー`の音を`再生`{:class="block3sound"}する前に、`こんにちは！`を`言います`{:class="block3looks"}。

```blocks3
    緑の旗がクリックされたとき
    言う [Hello]
    サウンドを再生する[meow v]
```

\--- /collapse \---

プログラムの不要なコードブロックを外すまたは削除するのは簡単です！ それらをコードブロックパレットに戻すだけです。

**注意:**それらをコードブロックパレットにドラッグすると、ドラッグしたブロックに接続されているすべてのブロックは削除されます。そのため、保持したいコードブロックと削除したいブロックを必ず別々にしてください。 誤って削除したコードブロックを取り戻したい場合は、 右クリックし**元に戻す**というオプションをクリックしてすべてを元に戻します。

![](images/code6.png)

\--- task \---

いくつかのコードブロックを追加、削除、削除解除をしてみてください！

\--- /task \---

### すべてを一緒に入れて

これでコードを移動して物事を実現する方法がわかったので、そろそろスクラッチキャットを丸く歩かせるプログラムを作成しましょう！

\--- task \---

スプライトリストにある猫のスプライトが選択されていることを確認し、次のブロックをスプライトパネルにドラッグして接続します。 ブロックは**イベント**と**動き**のリストから見つかりますよ。

```blocks3
    緑色の旗がクリックされたとき
    移動 [10] ステップ
```

\--- /task \---

\--- task \---

次に、ステージの上にある緑の旗をクリックします。

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