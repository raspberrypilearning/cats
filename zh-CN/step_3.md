## 克隆猫咪

您需要源源不断的生成猫咪来让玩家画出路径引导猫咪直到出口。

--- task ---

单击名为 "猫咪" 的精灵，然后添加代码来 `隐藏`{:class="block3looks"} 猫咪精灵，并每 3 秒 `克隆自己`{:class="block3control"}。

![猫咪精灵](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

--- /task ---

如果您现在运行程序，舞台上什么也不会发生。 要检查是否每 3 秒克隆了一个新的猫咪精灵，我们需要让猫咪显示出来并从天空中掉下来

--- task ---

添加代码，`当作为克隆体启动时`{:class="block3control"}，它应该`显示`{:class="block3looks"}，然后 `碰到颜色`{:class="block3sensing"} 为舞台上绘制的蓝色。

![猫咪精灵](images/cat-sprite.png)

--- hints ---
 --- hint ---

`当作为克隆体启动时`{:class="block3control"}，`显示`{:class="block3looks"} 精灵。 `重复执行直到`{:class="block3control"}`碰到颜色`{:class="block3motion"} 蓝色 `将 y 坐标增加`{:class="block3control"}`-2`

--- /hint ---

--- hint ---

以下是你需要的代码块：

```blocks3
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```

--- /hint ---

--- hint ---

你的代码应该是这样的：

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

--- /hint ------ /hints ---

--- /task ---

单击绿色小旗标志时，您应该看到每三秒钟一只新的猫咪从舞台的顶部掉下来。 蓝色的地板上应该有一大堆的猫咪

![掉落的猫咪](images/falling-cats.png)