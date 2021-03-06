## Клонування котів

Тобі потрібен нескінченний потік котів, яких гравець повинен скеровувати вздовж шляху до виходу.

--- task ---

Клацніи спрайт під назвою "Кіт" і додай код, щоб `сховати`{:class="block3looks"} спрайт, а також `створювати клон`{:class="block3control"} кожні три секунди.

![Спрайт "Кіт"](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

--- /task ---

Якщо ти зараз запустиш програму, на сцені нічого не відбуватиметься. Щоб перевірити, чи створюється новий клон із спрайту "Кіт" кожні три секунди, зроби так, щоб кожен клон з’являвся вгорі й падав вниз із неба.

--- task ---

Додай код до спрайту, щоб `коли він починав як клон`{:class="block3control"}, він мав `показатися`{:class="block3looks"} і падати доки не `торкнеться`{:class="block3sensing"} синьої підлоги, яка зображена на сцені.

![Спрайт "Кіт"](images/cat-sprite.png)

--- hints ---
 --- hint ---

`Коли спрайт починає як клон`{:class="block3control"}, `показати`{:class="block3looks"} спрайт. `Повторити`{:class="block3control"} `зміну`{:class="block3motion"} значення координати `y` спрайта на `-2`, поки він не `торкнеться`{:class="block3sensing"} на синьої частини сцени.

--- /hint ---

--- hint ---

Тобі будуть потрібні наступні блоки коду:

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

Ось як має виглядати твій код:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

--- /hint ------ /hints ---

--- /task ---

Після натискання на зелений прапорець, ти маєш побачити, як новий кіт падає з верхньої частини сцени кожні три секунди. Кожен кіт повинен приземлитися у велику купу котів на блакитній підлозі внизу.

![Падаючі коти](images/falling-cats.png)