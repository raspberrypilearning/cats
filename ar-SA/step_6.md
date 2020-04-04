## الوصول إلى بر الأمان

الهدف من اللعبة هو توجيه القطط نحو الأمان عن طريق إنشاء مسار حتى يمكنها الوصول إلى الباب. أنشئ متغير نتيجة لتسجيل كم قط استطاع الوصول إلى الباب.

--- task ---

أنشئ متغيراً يدعى `النتيجة`{:class="block3variables"}.

![كائن القط](images/cat-sprite.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

أضف تعليمات برمجية لكائن القط لإضافة `1` إلى `النتيجة`{:class="block3variables"} كل مرة يصل قط إلى الباب. أيضاً اجعل `النتيجة`{:class="block3variables"} تساوي `0` عند `النقر على العلم الأخضر`{:class="block3events"} في بداية اللعبة.

![كائن القط](images/cat-sprite.png)

--- hints ---
 --- hint ---

`إذا`{:class="block3control"} كان القط `يلامس كائن الباب`{:class="block3sensing"}، عندها `أضف 1 إلى النتيجة`{:class="block3variables"}.

--- /hint ---

--- hint ---

فيما يلي كتل التعليمات البرمجية الجديدة التي تحتاج إلى إضافتها إلى جزء `عندما أبدأ كنسخة`:

```blocks3
change [النتيجة v] by (1)

if <> then
end

<touching (باب v)?>

set [النتيجة v] to (0)
```

--- /hint ---

--- hint ---

و هذا ما يجب أن تبدو عليه التعليمات البرمجية الخاصة بك:

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
+   if <touching (باب v)?> then
        change [النتيجة v] by (1)
    end
end
delete this clone

when flag clicked
+ set [النتيجة v] to (0)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

أضف المزيد من التعليمات البرمجية بحيث عندما يصل كائن القط إلى الباب، يصدر القط صوت مواء 'meow' ويختفي بعدها.

![كائن القط](images/cat-sprite.png)

```blocks3
play sound (meow v)
delete this clone
```

--- /task ---