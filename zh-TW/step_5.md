## 讓貓咪沿著線走

您會注意到，如果在兩個平台間畫了一座矮橋或是一條向上的斜坡，貓咪還是最終會穿過平台而不是走在平台上呢！

![貓咪們走過平台](images/cat-walk-through-platform.png)

--- task ---

在貓咪的代碼中，在 `下個造型`{:class="block3looks"} 積木之前加入另一個迴圈。 這次，迴圈應告訴貓向上移動`2`直到它不碰到藍色為止。

![貓咪](images/cat-sprite.png)

--- hints ---
 --- hint ---

貓咪應該 `將 y 座標增加2`{:class="block3motion"}`重複無限次直到`{:class="block3motion"} 它`沒有`{:class="block3motion"}`碰到藍色`{:class="block3motion"} 為止。

--- /hint ---

--- hint ---

這是你需要的程式積木：

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

--- /hint ---

--- hint ---

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
end
delete this clone
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

點一下綠色旗幟，然後畫一條向上的斜線。 看看貓咪是否有沿著這條線走。

--- /task ---