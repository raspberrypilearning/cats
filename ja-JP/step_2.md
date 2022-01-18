## 線をかく

--- task ---

「ネコ！」という基本 (きほん) の Scratch プロジェクトを開きます。

**オンライン:** [scratch.mit.edu/projects/382878493](https://scratch.mit.edu/projects/382878493){:target="_blank"}から基本のプロジェクトを開きます。

Scratch アカウントを持っている場合、 **リミックス**をクリックしてプロジェクトをコピーできます。

**オフライン:** オフラインエディターで [基本のプロジェクト](https://rpf.io/p/ja-JP/cats-go)を開きます。 [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}から、Scratch オフラインエディターのダウンロードとインストールができます。

--- /task ---

--- task ---

プロジェクトにペン拡張機能 (かくちょうきのう) を追加 (ついか) します。

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

「ペン」というスプライトをクリックし、ペンの色をステージにあるしょうがいぶつと同じ青色にするコードを追加します。

![ペンスプライト](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

色を選択 (せんたく) するには、 `ペンの色を〜にする`{:class="block3extensions"}ブロックの色の四角をクリックし、マウスカーソルをピペットにかえ、ステージで正しい色をクリックします。

--- /task ---

--- task ---

スプライトをマウスポインターについていかせるために、さらにコードを追加します。 プログラムをテストして、コードがうまく動くかどうかをたしかめます。

![ペンスプライト](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

スプライトに、マウスボタンが押された (おされた) ときにステージ上に線をかくようにめいれいするコードを追加します。

![ペンスプライト](images/pen-sprite.png)

--- hints ---
 --- hint ---

`もし`{:class="block3control"}`マウスが押された`{:class="block3sensing"}なら、 `ペンを下ろし`{:class="block3extensions"}、`でなければ`{:class="block3control"}`ペンを上げます`{:class="block3extensions"}。

--- /hint ---

--- hint ---

必要なコードブロックは次のとおりです。

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

--- /hint ---

--- hint ---

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

--- /hint ---

--- /hints --- --- /task ---

--- task ---

コードをテストしましょう。 マウスでクリックしてドラッグすると、ステージに青い線をかくことができるはずです。

![線をかく](images/draw-a-line.png)

--- /task ---

ステージの右上にいつも青い点が出てくると思います (上の画像 ((がぞう)) では丸でかこまれています)。 これは、緑の旗 (はた) をクリックしてゲームを始めるときにマウスボタンをおすので、すぐにペンがかき始めるからです。

--- task ---

これをふせぐには、スクリプトの先頭に `ペンを上げる`{:class="block3extensions"}ブロックを追加し、 `ずっと`{:class="block3control"}ブロックの上に`1秒待つ`{:class="block3control"}ブロックを追加します。

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

--- /task ---
