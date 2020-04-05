## 画线

--- task ---

打开“猫！”的初始项目。

**在线版本:** 从这里 [scratch.mit.edu/projects/382880478](https://scratch.mit.edu/projects/382880478){:target="_blank"} 打开初始项目。

如果您有 Scratch 帐户，可以单击 **改编** 复制这个项目。

**离线版本:** 在离线编辑器中打开 [初始项目](http://rpf.io/p/zh-CN/cats-go)。 如果您需要下载并安装 Scratch 离线编辑器，可以点击链接获取[rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}。

--- /task ---

--- task ---

将 pen 扩展库添加到项目中。

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

单击名为 “笔” 的精灵，然后添加代码将笔的颜色设置为与舞台上的障碍物相同的蓝色。

![笔精灵](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

要选择一种颜色，请在 `将笔的颜色设置为`{:class="block3extensions"} 积木块中单击颜色块，在打开的弹窗中选择滴管工具并移动到舞台中的障碍物上，来获取正确的颜色

--- /task ---

--- task ---

添加更多代码来让精灵随着鼠标移动。 测试您的程序以检查代码是否有效。

![笔精灵](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

添加一些代码，告诉精灵如果按下鼠标按钮，则可以在舞台上画一条线。

![笔精灵](images/pen-sprite.png)

--- hints ---
 --- hint ---

`如果`{:class="block3control"}`按下鼠标?`{:class="block3sensing"}，则 `落笔`{:class="block3extensions"}，`否则`{:class="block3control"}，`抬笔`{:class="block3extensions"}。

--- /hint ---

--- hint ---

下面是你需要的代码块：

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

你的代码应该是这样的：

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

测试你的代码。 您应该能够单击并拖动鼠标在舞台上绘制蓝色的线。

![画一条线](images/draw-a-line.png)

--- /task ---

您可能会看到一个蓝点始终出现在舞台的右上角(在上图中被圈出)。 这是因为，当您单击绿色标志开始游戏时，您按下了鼠标，因此笔立即开始绘制。

--- task ---

为了阻止这种情况发生，在代码块开始的部分添加 `抬笔`{:class="block3extensions"} 和 `等待 1 秒`{:class="block3control"} 积木块，放在 `重复执行`{:class="block3control"} 积木块前面。

![笔精灵](images/pen-sprite.png)

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