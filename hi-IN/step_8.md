## मछली पकड़ना

शार्क चलती है, मछली तैरती है, लेकिन वे कुछ नहीं करते हैं: यदि मछली शार्क के मुंह में सही तैरती है, तो कुछ भी नहीं होता है। उसको बदलने का समय आ गया हैं!

सबसे पहले, आपको यह जानना होगा कि क्या मछली शार्क को छू रही है। इसके लिए, आपको **Control** ब्लॉक और एक **Sensing** ब्लॉक की आवश्यकता होगी।

--- task ---

**Control** श्रेणी से `if...then`{:class="block3control"} ब्लॉक को मछली स्प्राइट के `forever`{:class="block3control"} लूप के अंदर के `if on edge bounce`{:class="block3motion"} ब्लॉक के नीचे जोड़ें।

`touching...`{:class="block3sensing"} ब्लॉक को `if...then`{:class="block3control"} ब्लॉक के ऊपर के जगह में खींचे, और छोटे त्रिकोण को दबाकर शार्क स्प्राइट के नाम को चुनें। यदि आपने इसे नहीं बदला है, तो यह 'Sprite 1' होगा।

```blocks3
    when green flag clicked
    set rotation style [left-right v]
    forever 
        move (10) steps
        turn cw (pick random (1) to (10)) degrees
        wait (0.5) secs
        if on edge, bounce
+        if <touching [Sprite1 v] ?> then
    end
```

--- /task ---

--- collapse ---
---
title: यह कैसे काम करता है?
---

**Control** श्रेणी के `if...then`{:class="block3control"} ब्लॉक को `True/False` मूल्य दिया जाना चाहिए।

**Sensing** श्रेणी के ब्लॉक्स जानकारी एकत्र करते हैं, जैसे कि स्प्राइट कहां है, यह क्या छू रहा है, आदि। आप इस ब्लॉक का उपयोग कर रहे हैं:

```blocks3
    <touching [Sprite1 v] ?>
```

इस ब्लॉक के नुकीले सिरे से, आप बता सकते हैं कि यह आपको `True/False` का मान बताने जा रहा है जो `if...then`{:class="block3control"} ब्लॉक की जरूरत है।

--- /collapse ---

बेशक, आपने अभी `if...then`{:class="block3control"} ब्लॉक जोड़ा है लिकिन 'then' भाग के लिए कुछ भी जोड़े बिना। तो इस समय आपकी स्क्रिप्ट जाँच रही है कि क्या मछली स्प्राइट शार्क स्प्राइट को छू रही है, लेकिन यह प्रतिक्रिया में कुछ भी नहीं कर रही है।

आप `hide`{:class="block3looks"} ब्लॉक का इस्तमाल करके मछली को गायब कर सकते हैं, जैसे कि शार्क ने इसे खा लिया।

--- task ---

**Looks** श्रेणी में `hide`{:class="block3looks"} ब्लॉक को ढूंढ़े और इसे `if...then`{:class="block3control"} ब्लॉक के अंदर जोड़ें, जैसे इस तरह:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

--- /task ---

अब एक बार शार्क मछली को पकड़ लेती है, तो मछली गायब हो जाती है। यह अच्छा नहीं है।

--- task ---

**Looks** श्रेणी से `show`{:class="block3looks"} ब्लॉक को मछली कोड के शुरुआत में जोड़ें ताकि आप खेल को रीसेट कर सके।

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

--- /task ---

यह पहले से ही बेहतर है, लेकिन आप नहीं चाहते कि खिलाड़ी को हर बार एक ही मछली पकड़ने के लिए खेल को फिर से शुरू करना पड़े!

--- task ---

अपने `if...then`{:class="block3control"} ब्लॉक के अंदर के कोड को इस तरह दिखने के लिए अपडेट करें:

```blocks3
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
+        wait (1) secs
+        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
+        show
    end
```

--- /task ---

--- collapse ---
---
title: यह कैसे काम करता है?
---

आप यहाँ चतुर हो रहे हैं: जब मछली छिपी होती है, तो वह इंतजार करता है, चलता है, और फिर फिर से दिखाता है।

ऐसा लगता है कि बहुत सारी मछलियां दिखाई देती हैं, लेकिन यह है कि एक स्प्राइट चारों ओर घूम रहा है!

--- /collapse ---

यह एक खेल है! लेकिन अभी तक स्कोर बनाए रखने, या जीतने का कोई तरीका नहीं है। आप इसे भी ठीक कर सकते हैं - अगले कार्ड पर!