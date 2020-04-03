## 線をかく

\--- task \---

「ネコ！」という基本の Scratch プロジェクトを開きます。

**オンライン:** [rpf.io/cats-on](http://rpf.io/cats-on){:target="_blank"}から基本のプロジェクトを開きます。

Scratch アカウントを持っている場合、 **リミックス**をクリックしてプロジェクトをコピーできます。

**オフライン:** オフラインエディターで [基本のプロジェクト](http://rpf.io/p/en/cats-go)を開きます。 [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}から、Scratch オフラインエディターのダウンロードとインストールができます。

\--- /task \---

\--- task \---

プロジェクトにペン拡張機能 (かくちょうきのう) を追加 (ついか) します。

[[[generic-scratch3-add-pen-extension]]]

\--- /task \---

\--- task \---

「ペン」というスプライトをクリックし、ペンの色をステージにあるしょうがいぶつと同じ青色にするコードを入れます。

![ペンスプライト](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

色を選択 (せんたく) するには、 `ペンの色を〜にする`{:class = "block3extensions"}ブロックの色の四角をクリックし、マウスカーソルをピペットにかえ、ステージで正しい色をクリックします。

\--- /task \---

\--- task \---

Add some more code to make the sprite follow the mouse pointer. プログラムをテストして、コードがうまく動くかどうかをたしかめます。

![ペンスプライト](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

\--- /task \---

\--- task \---

Add some code to tell the sprite to draw a line on the Stage if the mouse button is pressed down.

![ペンスプライト](images/pen-sprite.png)

\--- hints \--- \--- hint \---

`If`{:class="block3control"} the `mouse is down`{:class="block3sensing"}, put the `pen down`{:class="block3extensions"}, and `else`{:class="block3control"}, lift the `pen up`{:class="block3extensions"}.

\--- /hint \---

\--- hint \---

必要なコードブロックは次のとおりです。

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

\--- /hint \---

\--- hint \---

コードは次のようになります。

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
forever
go to (mouse pointer v)
+ if <mouse down?> then
pen down
else
pen up
end
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

コードをテストしましょう。 マウスでクリックしてドラッグすると、ステージに青い線をかくことができるはずです。

![線を描く](images/draw-a-line.png)

\--- /task \---

You probably see that a blue dot always appears in the top right-hand corner of the Stage (it's circled in the image above). This is because, when you click the green flag to start the game, you press the mouse down, and so the pen immediately starts drawing.

\--- task \---

To stop this from happening, add a `pen up`{:class="block3extensions"} block at the start of the script, and a `wait one second`{:class="block3control"} block above the `forever`{:class="block3control"} block.

![ペンスプライト](images/pen-sprite.png)

```blocks3
when flag clicked
+ pen up
set pen color to [#0000ff]
erase all
set pen size to (5)
+ wait (1) seconds
forever
go to (mouse pointer v)
if <mouse down?> then
pen down
else
pen up
end
```

\--- /task \---