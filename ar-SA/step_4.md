## تحريك القطط

بمجرد أن تصل القطة إلى الأرض، يجب أن تتحرك ببطء إلى اليمين.

--- task ---

أضف تعليمات برمجية إلى جزء `عندما أبدأ كنسخة`{:class="block3control"} لتجعل كائن القط `يتحرك عشر خطوات`{:class="block3motion"}، وقم بالتبديل بين مظهري الكائن كل 0.1 ثانية لجعل القط يبدو وكأنه يمشي.

![كائن القط](images/cat-sprite.png)

--- hints ---
 --- hint ---

يجب على كائن القط أن `يتحرك 10 خطوات`{:class="block3motion"}، و`يبدل المظهر`{:class="block3looks"} كل `0.1 ثانية`{:class="block3control"}. هذه التعليمات يجب أن يتم تكرارها `باستمرار`{:class="block3control"}، تماماً مثل التعليمات التي تجعل القطط تتساقط.

--- /hint ---

--- hint ---

هنا التعليمات البرمجية التي ستحتاج اليها:

```blocks3
move (10) steps

wait (0.1) seconds

next costume

forever
end
```

--- /hint ---

--- hint ---

و هذا ما يجب أن تبدو عليه التعليمات البرمجية الخاصة بك:

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

اضغط على العلم الأخضر وتحقق من أن القطط تتحرك الآن على طول المنصة الزرقاء في الأسفل.

--- /task ---

إذا قمت برسم جسر عبر الفجوة بحيث تتمكن القطط من الوصول إلى الجانب الأيمن من المنصة، يمكنك أن ترى أنها ستنتهي في النهاية بالسير داخل الجدار الأيمن.

![القطط المتدفقة على الحافة](images/flailing-at-edge.png)

--- task ---

احذف حلقة `كرر باستمرار`{:class="block3control"}، وأضف بدلاً منها حلقة تكرار مختلفة تجعل القطط تستمر في المشي حتى تصل إلى أحد الحواف. عندما يصل القط إلى حافة المنصة، يجب أن يختفي.

![كائن القط](images/cat-sprite.png)

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

اضغط على العلم الأخضر وتحقق من اختفاء القطط عند وصولها إلى حافة المنصة.

--- /task ---

ستلاحظ أنه إذا سقطت القطط في الحفرة، فإنها لا تختفي بل ستظل عالقة في القاع. وهذا لأنها ستستمر بمحاولة السقوط إلى الأسفل.

هذا هو الجزء من التعليمات البرمجية الذي يطلب من القط الاستمرار في السقوط حتى تلامس اللون الأزرق:

```blocks3
repeat until <touching color [#0000ff]?>
end
```

مع ذلك، عند السقوط في الحفرة، لن يتمكن القط من بلوغ المنصة الرزقاء، لذلك سيكون عالقاً إلى الأبد.

--- task ---

أضف المزيد من الكتل البرمجية إلى هذه الحلقة بحيث يتم تكرارها حتى يلامس كائن القط المنصة الزرقاء `أو`{:class="block3operators"} `يلامس الحافة`{:class="block3sensing"}. بهذه الطريقة، سيتوقف القط عن محاولة السقوط عند الوصول إلى حافة المنصة.

![كائن القط](images/cat-sprite.png)

```blocks3
repeat until <<touching color [#0000ff]?> or <touching (edge v)?>>
end
```

--- /task ---