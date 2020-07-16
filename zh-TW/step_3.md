## 複製貓

您需要玩家引導這些源源不斷出現的貓群找到出口的路。

\--- task \---

點一下名為“ Cat”的角色，然後添加代碼來 `隱藏`{：class =“ block3looks”}角色，並每3秒`複製`{：class =“ block3looks”}它。

![貓角色](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

如果您現在執行程序，舞台上會什麼動靜也沒有。 要檢查是否每三秒鐘就出現一個新的複製貓，我們可以讓每隻分身都從天空出現掉下來。

\--- task \---

添加代碼以告知這角色，當它</code>{：class =“ block3control”}開始分身時 `，它應該要 <code>顯示`{：class =“ block3looks”}，然後一直下降到牠 `碰到`{：class =“ block3sensing“}畫在舞台上的藍色地板為止。

![貓角色](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`當角色作為分身`{：class =“ block3control”}開始時， `顯示`{：class =“ block3looks”}角色。 `重複`{：class =“ block3control”} `更改`{：class =“ block3motion”}這個角色的 `y` 坐標 `-2`，直到這個角色 `碰到`{：class =“ block3control”“}了藍色舞台。

\--- /hint \---

\--- hint \---

這裡是你需要的程式積木：

```blocks3
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```

\--- /hint \---

\--- hint \---

你的程式看起來應該像這樣：

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

點一下綠色旗幟時，您應該會每三秒鐘看到一隻新的貓從舞台上方掉下來。 每隻貓都應該都會掉在底部藍色地板上的那一大堆貓咪中。

![掉下來的貓咪](images/falling-cats.png)