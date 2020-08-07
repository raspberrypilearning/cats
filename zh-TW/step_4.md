## 讓貓咪動起來

當貓碰到地板後，它應該慢慢地向右前進。

--- task ---

添加代碼到 `當分身產生`{:class="block3control"} 這部分，讓貓咪 `移動十步`{:class="block3control"} ，然後每隔 0.1 秒從貓咪的兩種造型中切換一次，使它看起來像在走路一樣。

![貓咪](images/cat-sprite.png)

--- hints ---
 --- hint ---

貓咪應該要`移動10步`{:class="block3motion"}和每`0.1秒`{:class="block3control"}`切換到下個造型`{:class="block3looks"}。 這代碼應重複`重複無限次`{:class="block3control"}，就像使貓掉下來的代碼一樣。

--- /hint ---

--- hint ---

這是你需要的程式積木：

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

--- /hint ---

--- hint ---

你的程式看起來應該像這樣：

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

按下綠色旗幟，然後檢查貓咪現在是否有沿著底部的藍色平台移動。

--- /task ---

如果您在間隙上搭起一座橋樑，就能讓貓咪可以一直走到舞台的右側，您會發現它們最後都會卡在右邊的牆裡。

![在邊緣掙扎的貓咪](images/flailing-at-edge.png)

--- task ---

移除`重複無限次`{:class="block3control"}迴圈，然後添加一個不同的迴圈使貓咪只走到當它們到達邊緣為止。 當貓咪到達舞台邊緣時，它應該要消失。

![貓咪](images/cat-sprite.png)

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

按下綠色旗幟，並檢查貓咪們走到舞台邊緣時是否有消失。

--- /task ---

您可能有注意到，如果貓掉入洞中，它們不會消失，而是會卡在底部。 這是因為他們一直不斷試圖著往下掉。

這是原代碼的一部分，讓貓一直一直往下掉到它碰到藍色才停止：

```blocks3
repeat until <touching color [#0000ff]?>
end
```

但是，在洞中，貓永遠無法到達藍色，因此它會一直卡住。

--- task ---

在這重複無限次區塊中加入更多積木，讓它能重複執行直到碰到藍色 `或`{:class="block3operators"}, `碰到舞台邊緣`{:class="block3sensing"}。 這樣一來，如果貓咪到了舞台的邊緣，它就會停止繼續往下掉。

![貓咪](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

--- /task ---