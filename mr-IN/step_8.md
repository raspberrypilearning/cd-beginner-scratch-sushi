## मासेमारी!

शार्क फिरतो, मासे पोहतात, परंतु ते परस्पर संवाद साधत नाहीत: जर माशा शार्कच्या तोंडात पोहायला लागला तर काहीही होत नाही. ते बदलण्याची वेळ!

प्रथम, आपल्याला हे माहित असणे आवश्यक आहे की मासा शार्कला स्पर्श करीत आहे की नाही. यासाठी, आपल्याला **Control** ब्लॉक आणि **Sensing** ब्लॉक लागणार आहे.

--- task ---

फिश स्प्राइटच्या `forever`{:class="block3control"} लूपमध्ये `if on edge bounce`{:class="block3motion"} ब्लॉकच्या खाली `if...then`{:class="block3control"} **Control** ब्लॉक जोडा.

`if...then`{:class="block3control"} ब्लॉकच्या शीर्षस्थानी असलेल्या जागेमध्ये `touching...`{:class="block3sensing"} ब्लॉक ड्रॅग करा आणि शार्क स्प्राइटचे नाव निवडण्यासाठी लहान त्रिकोण क्लिक करा. आपण ते बदलले नसल्यास ते 'Sprite 1' असेल.

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
title: हे कसे कार्य करते?
---

`if...then`{:class="block3control"} **Control** ब्लॉकला `True/False` मूल्य दिले जाणे आवश्यक आहे.

**Sensing** ब्लॉक्स माहिती गोळा करतात, जसे की स्प्राइट कोठे आहे, ते काय स्पर्श करीत आहे इ. आपण हा ब्लॉक वापरत आहात:

```blocks3
    <touching [Sprite1 v] ?>
```

या ब्लॉकच्या टोकांच्या शेवटपर्यंत, आपण हे सांगू शकता की आपल्याला `if...then`{:class="block3control"} ब्लॉकला आवश्यक असलेले `True/False` मूल्य दिले जाईल.

--- /collapse ---

नक्कीच, आपण 'then' भागासाठी काहीही न जोडता फक्त एक `if...then`{:class="block3control"} ब्लॉक जोडला आहे. म्हणून याक्षणी आपली स्क्रिप्ट फिश स्प्राइट शार्कच्या बाजूस स्पर्श करीत आहे की नाही ते तपासत आहे, परंतु प्रतिसादात काही घडत नाही.

`hide`{:class="block3looks"} ब्लॉक वापरुन आपण शार्कने खाल्ल्याप्रमाणे मासे अदृश्य करू शकता.

--- task ---

**Looks** सूचीतील `hide`{:class="block3looks"} ब्लॉक शोधा आणि त्यास `if...then`{:class="block3control"} ब्लॉकमध्ये ठेवा:

```blocks3
    if <touching [Sprite1 v] ?> then
+        hide
    end
```

--- /task ---

आता एकदा शार्कने मासा पकडल्यावर मासा कायमचा अदृश्य होतो. ते उत्तम नाही.

--- task ---

फिश कोडच्या अगदी सुरुवातीस **Looks** मधील `show`{:class="block3looks"} ब्लॉक ठेवा, म्हणजे आपण गेम रीसेट करू शकता.

```blocks3
    when green flag clicked
+    show
    set rotation style [left-right v]
    forever
```

--- /task ---

ते आधीपासूनच चांगले आहे, परंतु प्रत्येक वेळी एकच मासा पकडतांना प्रत्येक वेळी तो खेळ पुन्हा सुरू करावा अशी तुमची इच्छा नाही!

--- task ---

असे दिसण्यासाठी आपल्या `if...then`{:class="block3control"} ब्लॉकमधील कोड अद्यतनित करा:

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
title: हे कसे कार्य करते?
---

आपण येथे हुशार आहात: जेव्हा मासा लपविला जातो तेव्हा तो थांबतो, फिरतो, आणि पुन्हा दर्शविला जातो.

असे दिसते की बरीच मासे दिसू लागली आहेत, परंतु तो एक स्प्राइट फिरत आहे!

--- /collapse ---

तो एक खेळ आहे! परंतु अद्याप स्कोअर ठेवण्याचा किंवा जिंकण्याचा कोणताही मार्ग नाही. आपण हे देखील निश्चित करू शकता - पुढील कार्डवर!