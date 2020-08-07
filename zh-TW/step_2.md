## 畫線

--- task ---

打開“貓！”Scratch入門項目。

**線上版：**你可以點擊此 [scratch.mit.edu/projects/416381159](https://scratch.mit.edu/projects/416381159){:target="_blank"} 開啟入門項目。

如果你有 Scratch 帳戶，你就可以直接**改編**專案。

**離線：** 在離線編輯器中打開 [入門項目](http://rpf.io/p/zh-TW/cats-go)。 如果你需要 Scratch 離線版編輯器，可以連結到 [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}。

--- /task ---

--- task ---

把畫筆這個擴充功能加入到專案裡。

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

點一下名為“鉛筆”的角色，然後加入以下程式碼將筆的顏色設為與舞台上的障礙物相同的藍色。

![筆角色](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

如要選擇一種顏色，請在 `筆跡顏色設為`{:class="block3extensions"}積木中單擊顏色方塊，當滑鼠游標變成吸管，就可以在舞台上點取物品找到你要的正確顏色。

--- /task ---

--- task ---

加入更多程式碼讓這角色能跟著鼠標走。 測試您的程序以檢查程式代碼是否有效。

![筆角色](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

添加一些程式代碼，告訴這角色如果按下鼠標按鈕，就可以在舞台上畫一條線。

![筆角色](images/pen-sprite.png)

--- hints ---
 --- hint ---

`如果`{:class="block3control"} `滑鼠鍵被按下`{:class="block3sensing"}，則放入 `下筆`{:class="block3extensions"}，`否則`{:class="block3control"}，使用`停筆`{:class="block3extensions"}。

--- /hint ---

--- hint ---

這裡是你需要的程式積木：

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

你的程式看起來應該像這樣：

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

測試你的程式。 您應該能夠單擊並拖曳鼠標在舞台上繪製藍線。

![畫一條線](images/draw-a-line.png)

--- /task ---

您可能會看到一個藍點始終出現在舞台的右上角（被圈出的藍點如上圖所示）。 這是因為，當您單擊綠色旗幟開始遊戲時，您按下了鼠標，因而筆立即開始繪製的動作。

--- task ---

為了避免這種情況發生，可添加 `停筆`{:class="block3extensions"}積木在程式區腳本的開頭和一塊`等待1秒鐘`{:class="block3control"}積木塊，這積木在 `重複無限次`{:class="block3control"}積木的上面。

![筆角色](images/pen-sprite.png)

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