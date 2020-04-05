## 让猫咪动起来

一旦猫咪到达地面，它就应慢慢向右边走。

--- task ---

添加代码到 `当作为克隆体启动时`{:class="block3control"} ，使猫咪精灵 `移动 10 步`{:class="block3control"} 并且 每隔 0.1 秒在猫咪精灵的两个造型之间切换，来让猫咪看起来像在走路。

![猫咪精灵](images/cat-sprite.png)

--- hints ---
 --- hint ---

猫咪精灵应该 `移动 10 步`{:class="block3motion"} 并且每 `0.1秒`{:class="block3motion"} 切换 `下一个造型`{:class="block3motion"} 。 这个代码应该和猫咪下落的代码一样在 `重复执行`{:class="block3control"}积木块里。

--- /hint ---

--- hint ---

以下是你需要的代码块：

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

--- /hint ---

--- hint ---

你的代码应该是这样的：

```blocks3
when I start as a clone
show
+ forever
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

按下绿色小旗标志，然后检查猫现在是否沿着底部的蓝色平台移动。

--- /task ---

如果您在间隙上通过画线架起一座桥，来让猫咪可以一直走到舞台的右侧，您会发现它们最终被困在右墙中。

![在边缘挣扎的猫咪](images/flailing-at-edge.png)

--- task ---

删除 `重复执行`{:class="block3control"} 循环，替换为一个 重复执行直到碰到舞台边缘 的循环积木块。 当猫咪到达舞台边缘时，它应该消失。

![猫咪精灵](images/cat-sprite.png)

```blocks3
when I start as a clone
show
+ repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) seconds
end
+ delete this clone
```

--- /task ---

--- task ---

按下绿色小旗标志，并检查猫咪到达舞台边缘时是否消失。

--- /task ---

您可能会注意到，如果猫掉入洞中，它们不会消失，而会卡在底部。 这是因为他们不断试图向下下滑。

这是代码的一部分，它告诉猫继续跌落，直到它碰到蓝色：

```blocks3
repeat until <touching color [#0000ff]?>
end
```

但是，在洞中，猫永远无法到达蓝色，因此它会一直被卡住。

--- task ---

向此循环添加更多块，重复执行直到碰到颜色蓝色 `或`{:class="block3operators"}, `碰到舞台边缘`{:class="block3sensing"}。 这样，如果精灵到达舞台的边缘，它将停止尝试掉落。

![猫咪精灵](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

--- /task ---