## 让猫保持安全

游戏的目标是通过绘制一条路径引导猫咪保持安全，这样他们就可以到达门型出口。 创建一个 分数 变量以跟踪有多少只猫到达了门口。

--- task ---

创建一个新的名为 `分数`{:class="block3variables"} 的变量

![猫咪精灵](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

添加代码，每次当有猫咪到达门口时，将`分数`{:class="block3variables"} 增加 `1`。 同时在 `当绿旗被点击`{:class="block3events"} 将 `分数`{:class="block3variables"} 设为 `0`。

![猫咪精灵](images/cat-sprite.png)

--- hints ---
 --- hint ---

`如果`{:class="block3control"} 猫咪精灵 `碰到门`{:class="block3sensing"}，`将 分数 增加 1`{:class="block3variables"}。

--- /hint ---

--- hint ---

下面是你需要添加到`当作为克隆体启动时` 代码块的代码：

```blocks3
change [分数 v] by (1)

if <> then
end

<touching (门 v)?>

set [分数 v] to (0)
```

--- /hint ---

--- hint ---

你的代码应该是这样的：

```blocks3
when I start as a clone
show
repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    repeat until <not <touching color [#0000ff]?>>
        change y by (2)
    end
    next costume
    wait (0.1) seconds
+   if <touching (门 v)?> then
        change [分数 v] by (1)
    end
end
delete this clone

when flag clicked
+ set [分数 v] to (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

添加更多代码，以便当猫咪精灵到达门口时，发出 “meow” 的声音，然后消失。

![猫咪精灵](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

--- /task ---