## صيد السمك!

يتحرك سمك القرش ، السمكة تسبح ، لكنهما لا يتفاعلان: إذا كانت السمكة تسبح مباشرة في فم القرش ، فلن يحدث شيء. حان الوقت لتغيير ذلك!

أولاً ، تحتاج إلى معرفة ما إذا كانت السمكة تلامس سمك القرش. لهذا ، ستحتاج إلى مقطع ** التحكم ** و مقطع** الاستشعار **.

\--- task \--- أضف مقطع **التحكم** `إذا`{:class="block3control"} داخل مقطع `كرر باستمرار`{:class="block3control"} لكائن السمكة بعد مقطع `ارتد إذا كنت عند الحافة`{:class="block3motion"}.

اسحب مقطع `ملامس ل...`{:class="block3sensing"} الى المسافة التي في مقطع `اذا` وانقر على المثلث الصغير واختر اسم كائن سمكة القرش. إذا لم تقم بتغييرها ، فستكون "Sprite1".

```blocks3
    عند نقر العلم الأخضر 
    اجعل نمط الدوران  [يمين - يسار v]
    كرر باستمرار
        تحرك (10) خطوة
        استدر مع عقارب الساعة (عدد عشوائي بين (1) و (10)) درجات
        انتظر (0.5) ثانية
        ارتد إذا كنت عند الحافة
+        إذا<touching [Sprite1 v] ?>
    النهاية
```

\---/task--

## \--- collapse \---

## title: كيف يعمل؟

مقطع **التحكم** `إذا`{:class="block3control"} يحتاج إلى قيمة `صواب / خطأ`.

مقاطع ** الاستشعار ** تقوم بتجميع المعلومات ، مثل مكان الكائن ، ما الذي يلامسه ، إلخ. أنت تستخدم هذه الكتلة:

```blocks3
    <touching [Sprite1 v] ?>
```

من النهايات المدببة لهذا المقطع ، يمكنك معرفة أنه سيعطيك قيمة ` صواب / خطأ ` التي يحتاجها مقطع ` إذا...` {: class="block3control"}.

\--- /collapse \---

بالطبع ، لقد أضفت للتو مقطع ` إذا...`{: class="block3control"} دون إضافة أي شيء فيه. لذا في الوقت الحالي ، يقوم البرنامج النصي بالتحقق مما إذا كان كائن السمكة يلامس كائن سمك القرش ، لكنه لا يعمل أي شيئ لذلك.

يمكنك جعل السمكة تختفي ، كما لو أن سمك القرش أكلها ، باستخدام مقطع `إختفِ` {:class= "block3looks"}.

ابحث عن مقطع `إختفِ`{:class="block3looks"} في قائمة **المظاهر**، وضعها بداخل مقطع `إذا...`، هكذا:

```blocks3
    إذا <touching [Sprite1 v] ?>
+        اختفِ
    النهاية
```

\--- /task \---

الآن بمجرد أن يصطاد سمكة القرش السمكة ، تختفي السمكة نهائيا. هذا ليس جيداً.

\--- task \--- Put the `show`{:class="block3looks"} block from **Looks** in at the very start of the fish code, so you can reset the game.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

\--- /task \---

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish!

\--- task \--- Update the code inside your `if...then`{:class="block3control"} block to look like this:

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

\--- /task \---

## \--- collapse \---

## title: How does this work?

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again.

It looks like lots of fish keep appearing, but it’s that one sprite moving around!

\--- /collapse \---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!