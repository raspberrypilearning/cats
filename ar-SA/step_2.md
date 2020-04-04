## رسم الخطوط

--- task ---

افتح مشروع سكراتش المبدئي "القطط!".

**بالاتصال بالانترنت:** افتح المشروع المبدئي من هنا [scratch.mit.edu/projects/382693982(https://scratch.mit.edu/projects/382693982){:target="_blank"}.

اذا كنت تملك حساب على منصة سكراتش (Scratch) فيمكنك عمل نسخة بالنقر على **مزج**.

**دون اتصال بالانترنت:** افتح [المشروع المبدئي](http://rpf.io/p/ar-SA/cats-go) عبر المحرر الموجود على جهازك. اذا تحتاج تنزيل وتنصيب برنامج السكراتش Scratch على جهازك الشخصي، ستجده في [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

أضف ملحق القلم لمشروعك.

[[[generic-scratch3-add-pen-extension]]]

--- /task ---

--- task ---

انقر على الكائن المسمى 'القلم'، وأضف تعليمة برمجية لتعيين لون القلم إلى نفس اللون الأزرق كالعقبات على المنصة.

![كائن القلم](images/pen-sprite.png)

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
```

لتحديد لون، انقر فوق مربع اللون في كتلة `تعيين لون القلم`{:class="block3extensions"} لتحويل مؤشر الماوس إلى انبوب، ثم انقر فوق اللون الصحيح في المنصة.

--- /task ---

--- task ---

قم بإضافة المزيد من التعليمات البرمجية لجعل الكائن بتبع مؤشر الماوس. اختبر برنامجك للتحقق من عمل البرنامج.

![كائن القلم](images/pen-sprite.png)

```blocks3
forever
go to (mouse pointer v)
end
```

[[[generic-scratch3-saving]]]

--- /task ---

--- task ---

أضف بعض التعليمات البرمجية لجعل الكائنات ترسم خط على المنصة إذا تم الضغط على زر الماوس.

![كائن القلم](images/pen-sprite.png)

--- hints ---
 --- hint ---

`إذا`{:class="block3control"} كان `زر الفأرة مضغوط`{:class="block3sensing"}, `أنزل القلم`{:class="block3extensions"}, and `وإلا`{:class="block3control"}, `ارفع القلم`{:class="block3extensions"}.

--- /hint ---

--- hint ---

هنا التعليمات البرمجية التي ستحتاج اليها:

```blocks3
<mouse down?>

pen down

pen up

if <> then
else
end
```

--- /hint ---

--- hint ---

و هذا ما يجب أن تبدو عليه التعليمات البرمجية الخاصة بك:

```blocks3
when flag clicked
set pen color to [#0000ff]
erase all
set pen size to (5)
forever
go to (mouse pointer v)
+ if <mouse down?> then
pen down
else
pen up
end
```

--- /hint ---

--- /hints --- --- /task ---

--- task ---

اختبر مشروعك. يجب أن تكون قادرًا على النقر والسحب بالماوس لرسم خط أزرق على المنصة.

![ارسم خطاً](images/draw-a-line.png)

--- /task ---

ربما ستظهر نقطة رزقاء بشكل دائم في الزاوية العلوية اليمنى من المنصة (النقطة المحاطة بدائرة في الصورة). هذا لأنه عندما تنقر على العلم الأخضر لبدء اللعبة، فإنك قمت بالضغط على زر الماوس، وبالتالي يبدأ القلم في الرسم على الفور.

--- task ---

لمنع حدوث ذلك، أضف كتلة `ارفع القلم`{:class="block3extensions"} في بداية البرنامج، وكتلة `انتظر 1 ثانية`{:class="block3control"} قبل كتلة `كرّر باستمرار`{:class="block3control"}.

![كائن القلم](images/pen-sprite.png)

```blocks3
when flag clicked
+ pen up
set pen color to [#0000ff]
erase all
set pen size to (5)
+ wait (1) seconds
forever
go to (mouse pointer v)
if <mouse down?> then
pen down
else
pen up
end
```

--- /task ---