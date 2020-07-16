## 安全抵達

遊戲的目標是畫出一條路徑引導貓咪讓他們能夠平安到達出口的門。 建立一個計分的變數來紀錄有多少隻貓咪到達了門口。

\--- task \---

建立一個新的變數，稱作`得分`{:class="block3variables"}。

![貓咪](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

添加代碼，每當有一隻貓咪到達門口時，`分數`{:class="block3variables"} 就加 `1`分。 同時在`點擊綠色旗幟開始遊戲` {：class =“ block3events”}時將`分數` {：class =“ block3variables”}歸` 0 ` 。

![貓咪](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`如果` {：class =“ block3control”}貓咪`碰到了門` {：class =“ block3sensing”}，將分數`加1 ` {：class =“ block3variables”}。

\--- /hint \---

\--- hint \---

下面是你需要添加到`當分身產生` 區塊的代碼：

```blocks3
change [score v] by (1)

if <> then
end

<touching (Door v)?>

set [score v] to (0)
```

\--- /hint \---

\--- hint \---

你的程式看起來應該像這樣：

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
+   if <touching (Door v)?> then
        change [score v] by (1)
    end
end
delete this clone

when flag clicked

+ set [score v] to (0)
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

添加更多代碼，以便讓貓咪到達門時，會發出“喵”的聲音，然後消失。

![貓咪](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

\--- /task \---