## Adding and removing code blocks

Great! You’ve written your very first Scratch program. Time to learn a little more about getting code in and out of Scratch! Scratch code is made up of **blocks** such as these:

![](images/code1.png)

आपको सभी ब्लॉक **code blocks palette** उनके अनुसार विभिन्न श्रेणियों में क्रमबद्ध।

## \--- collapse \---

## title: Using blocks from the different categories

Click on a category name to see the blocks in that category. यहाँ, ** Motion** श्रेणी चयनित है:

![](images/code2a.png)

आपके द्वारा क्लिक की गई श्रेणी के सभी ब्लॉक सूची में दिखाए गए हैं:

![](images/code2b.png)

You can click on the blcok you want, and then just drag it into the current sprite panel and let go. Once it's in the panel, you can move it around and connect it to other blocks.

\--- /collapse \---

If you want to see what a block does, you can double-click on it to make it run!

\--- task \---

कुछ ब्लॉकों पर डबल क्लिक करके देखें कि वे क्या करते हैं।

\--- /task \---

## \--- collapse \---

## title: Running the code

Usually, you want your code to run automatically whenever something specific happens. This is why many of your programs will start with a block from the **Events** category, most often this one:

```blocks3
    when green flag clicked
```

The code blocks connected to this block will run after the **green flag** is clicked.

Code blocks run from top to bottom, so the order in which you snap your blocks together matters. In this example, the sprite will `say`{:class="block3looks"} `Hello!` before it will `play`{:class="block3sound"} the `meow` sound.

```blocks3
    when green flag clicked
    say [Hello]
    play sound [meow v]
```

\--- /collapse \---

Removing or deleting code blocks you don’t want in your program is easy! Just drag them back into the code blocks palette.

** सावधान रहें: ** कोड ब्लॉक में उन्हें खींचने से आपके द्वारा खींचे जाने वाले ब्लॉक से जुड़े सभी ब्लॉक हट जाएंगे, इसलिए उन कोड ब्लॉक को अलग करना सुनिश्चित करें जिन्हें आप हटाना चाहते हैं। यदि आप दुर्घटना से कुछ कोड ब्लॉक हटाते हैं और उन्हें वापस लाना चाहते हैं, तो राइट-क्लिक करें और फिर **undo** सब कुछ वापस पाने का विकल्प।

![](images/code6.png)

\--- task \---

कुछ कोड ब्लॉक जोड़ने, हटाने और हटाने का प्रयास करें!

\--- /task \---

### इस सब को एक जगह लाना

अब आप जानते हैं कि कोड को कैसे घुमाया जाए और चीजों को कैसे बनाया जाए, यह आपके लिए एक सर्कल में स्क्रैच कैट वॉक करने का प्रोग्राम बनाने का समय है!

\--- task \---

सुनिश्चित करें कि आपके पास स्प्राइट सूची में चयनित बिल्ली स्प्राइट है, और फिर स्प्राइट पैनल में निम्नलिखित ब्लॉकों को खींचें और उन्हें कनेक्ट करें। आप उन्हें **Events** और **Motion** सूचियों ईवेंट में खोजेंगे ।

```blocks3
    when green flag clicked
    move [10] steps
```

\--- /task \---

\--- task \---

अब, स्टेज के ऊपर हरे झंडे पर क्लिक करें।

![](images/code7.png)

\--- /task \---

आपको बिल्ली को एक सीधी रेखा में चलते हुए देखना चाहिए ... ठीक वही नहीं जो आप चाहते हैं, है ना?

नोट: यदि आप कई बार ध्वज पर क्लिक करते हैं और बिल्ली दूर चली जाती है, तो आप उसे वापस खींच सकते हैं!

\--- task \---

एक सर्कल में बिल्ली को स्प्राइट चलने के लिए मोड़ ब्लॉक को अंत तक स्नैप करें। यह **Motion** सूची में है।

```blocks3
    when green flag clicked
    move [10] steps
+    turn cw (15) degrees
```

\--- /task \---

## \--- collapse \---

## शीर्षक: यह कैसे काम करता है?

यह ब्लॉक पूर्ण 360 डिग्री वाले स्प्राइट टर्न को 15 डिग्री बनाता है जो एक सर्कल बनाता है। नंबर पर क्लिक करके और नए मूल्य में टाइप करके आप उस नंबर और चरणों की संख्या को बदल सकते हैं।

![](images/code9.png)

\--- /collapse \---

\--- task \---

अब अपना काम बचाओ!

\--- /task \---