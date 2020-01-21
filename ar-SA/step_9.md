## حفظ النتيجة

للحفاظ على عدد الأسماك التي يصطادها اللاعب ، ستحتاج إلى مكان لتخزين النتيجة ، وطريقة إضافتها ، وطريقة لإعادة ضبطها عند إعادة تشغيل اللعبة.

أولاً: تخزين النتيجة!

\--- task \---

Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

Enter `score` as the name.

![](images/catch6.png)

Check out your new variable!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

\--- /task \---

## \--- collapse \---

## title: ما هي المتغيرات؟

When you want to store information in a program, you use something called a **variable**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. You’ll find variables in the **Variables** section, but you need to create them first for them to show up there!

\--- /collapse \---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. Doing both is pretty easy:

\--- task \---

From the **Variables** section, take the `set [my variable v] to [0]`{:class="block3variables"} and `change [my variable v] by [1]`{:class="block3variables"} blocks. Click on the little arrows in the blocks, choose `score` from the list, and then put the blocks into your program:

### بزمجة سمكة القرش

```blocks3
    عند نقر العلم الأخضر
+     اجعل [النتيجة v] مساوياً [0]
    اجعل نمط الدوران [يمين - يسار v]
    اذهب الى الموضع س: (0) ص: (0)
```

### برمجة السمكة

```blocks3
    إذا<touching [Sprite1 v] ?>
+        غير [النتيجة v] بمقدار [1]
        إخفِ
        انتظر (1) ثانية 
        اذهب إلى الموضع س: (عدد عشوائي (-240) الى (240)) ص: (عدد عشوائي (-180) الى (180))
        اظهر
    النهاية
```

\--- /task \---

Cool! Now you’ve got a score and everything.