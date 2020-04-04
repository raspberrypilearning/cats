## 让猫咪沿着线行走

您可能会注意到，如果您在两个平台之间画了一座稍微低一些的桥， 或者一条向上倾斜的直线，猫最终会在平台或线上穿行而不是走在它们上面！

![小猫咪们走过平台](images/cat-walk-through-platform.png)

\--- task \---

在猫咪精灵的代码中，在 `下一个造型`{:class="block3looks"} 积木块之前添加另一个循环。 这一次，循环应该告诉猫咪上移 `2` 步直到它不触碰蓝色。

![猫咪精灵](images/cat-sprite.png)

\--- hints \--- \--- hint \---

猫咪应该 `重复执行直到`{:class="block3motion"} `碰到颜色 蓝色`{:class="block3motion"} `不成立`{:class="block3motion"} `将 y 坐标增加2 `{:class="block3motion"}。

\--- /hint \---

\--- hint \---

以下是你需要的代码块：

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

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
end
delete this clone
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

单击绿色小旗标志，然后尝试绘制一条向上倾斜的线。 请检查您的猫是否跟随这条线。

\--- /task \---