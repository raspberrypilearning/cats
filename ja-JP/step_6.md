## 安全な場所へ

ゲームの目的は、ネコがドアに着けるように道を作って安全な場所へみちびくことです。 ドアに着いたネコの数をきろくするスコア変数 (へんすう) を作りましょう。

--- task ---

`スコア`{:class="block3variables"}という名前の変数を作りましょう。

![ネコのスプライト](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

ネコのスプライトに、ネコがドアに着くたびに`スコア`{:class="block3variables"}に`1`を足すコードを追加します。 また、ゲームを始めるときに`旗がクリックされたとき`{:class="block3events"}、`スコア`{:class="block3variables"}を`0`にするようにします。

![ネコのスプライト](images/cat-sprite.png)

--- hints ---
 --- hint ---

`もし`{:class="block3control"}ネコが`ドアのスプライトに触れている`{:class="block3sensing"}なら、`スコアに1を足します`{:class="block3variables"}。

--- /hint ---

--- hint ---

`クローンされたとき`スクリプトに追加する新しいコードブロックです。

```blocks3
change [スコア v] by (1)

if <> then
end

<touching (ドア v)?>

set [スコア v] to (0)
```

--- /hint ---

--- hint ---

コードは次のようになります。

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
+   if <touching (ドア v)?> then
        change [スコア v] by (1)
    end
end
delete this clone

when flag clicked
+ set [スコア v] to (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

ネコのスプライトがドアに着いたときに「ニャー」という音を出して消えるように、さらにコードを追加します。

![ネコのスプライト](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

--- /task ---