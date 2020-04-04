## الالتزام بالخطوط

قد تلاحظ أنه عند رسم جسر منخفض بين المنصتين، أو خط منحدر نحو الأعلى، ستقوم القطط بالمشي عبر المنصات الزرقاء بدلاً من المشي فوقها!

![القطط تمشي عبر المنصة](images/cat-walk-through-platform.png)

--- task ---

في التعليمات البرمجية الخاصة بكائن القط، أضف حلقة تكرار جديدة قبل كتلة `المظهر التالي`{:class="block3looks"}. هذه المرة، يجب أن تقوم هذه الحلقة بجعل القط يتحرك إلى الأعلى بمقدار `2` إلى أن لا يكون ملامساً للون الأزرق.

![كائن القط](images/cat-sprite.png)

--- hints ---
 --- hint ---

يجب على القط أن `يتحرك للأعلى بمقدار 2`{:class="block3motion"} `بشكل متكرر حتى`{:class="block3control"} يصبح `لا`{:class="block3operators"} `ملامساً للأزرق`{:class="block3sensing"}.

--- /hint ---

--- hint ---

هنا التعليمات البرمجية التي ستحتاج اليها:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
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
end
delete this clone
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

انقر على العلم الأخضر وحاول رسم خط ينحدر إلى الأعلى. تحقق من أن القط يتبع هذا الخط.

--- /task ---