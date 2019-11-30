## كل الكائنات

الآن لديك سمكة قرش يمكنها التنقل باستخدام مفاتيح الأسهم. رائع! حان الوقت لإضافة بعض الأسماك ليصطادها.

\--- task \---

انقر فوق زر **كائن جديد**، وعلى الشاشة التي تفتح ، اختر سمكة.

![The New sprite button](images/spritesNewFromLibrary.png)

إذا كانت أسماكك كبيرة بعض الشيء مقارنة بسمك القرش الخاص بك، فيمكنك استخدام التحكم في الحجم لجعل كل الكائنات بالحجم المناسب!

![Sprite size control](images/sprites2.png)

غير الرقم في خانة الحجم لجعل الكائن أكبر أو أصغر.

\--- /task \---

عظيم! في وقت لاحق ، ستقوم بإضافة بعض التعليمات البرمجية لجعل الأسماك تتحرك من تلقاء نفسها ، دون مساعدة من اللاعب. سيحرك اللاعب القرش ويحاول أن يصطاد السمك.

## \--- collapse \---

## title: وماذا عن القرش المعكوس؟

يبدو الأمر مضحكا بعض الشيء أن يكون هذا القرش يسبح للوراء. تمامًا كما أنت في العادة تستدير بدلا من ان تمشي للخلف ، فإن القرش يستدير بدلا من السباحة للخلف. لحسن الحظ ، Scratch لديه مقطع لهذا!

يتيح لك مقطع `اتجه نحو الاتجاه`{: class="block3motion"} اختيار الاتجاه الذي يشير إليه الكائن. ستجده في قسم مقاطع ** الحركة **. يمكنك كتابة أي مقدار من الدرجات ، لتوجيه الكائن أينما تريد. \--- /collapse \---

\--- task \--- احصل على نسختين من مقطع `اتجه نحو الاتجاه` {: class="block3motion"} من قائمة ** الحركة ** واربطهم ببرمجة القرش ، هكذا:

```blocks3
    عندما ضغط مفتاح [السهم الأيسر v] 
+ اتجه نحو الاتجاه (-90) 
    تحرك (10) خطوة
```

```blocks3
    عندما ضغط مفتاح [السهم الأيمن v]
+ اتجه نحو الاتجاه (90)
     تحرك (10) خطوة
```

\--- /task \---

\--- task \--- Change the number of steps in the `move`{:class="block3motion"} blocks from `-10` to `10`.

If you try moving the shark around now after you've added the `point in direction`{:class="block3motion"} blocks, you might notice something a little strange happening. The shark may not be turning quite right!

![Upside down shark](images/spritesUpsideDown.png)

\--- /task \---

## \--- collapse \---

## title: Why does it go upside down?

The problem here is that the shark sprite started, as all sprites do, with the 'all around' **rotation style**, and what you need it to have is the 'left-right' style.

As usual, there’s a block for that, and it’s in **Motion**!

\--- /collapse \---

\--- task \--- Look in the **Motion** category for the block `set rotation style`{:class="block3motion"}.

Add the block to your shark reset code from earlier, and set the rotation style to `left-right`{:class="block3motion"}, like this:

```blocks3
    when green flag clicked
+     set rotation style [left-right v]
    go to x: (0) y: (0)
```

\--- /task \---