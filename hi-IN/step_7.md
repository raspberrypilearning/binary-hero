## अधिक कस्टम ब्लॉक्स

कोड का नवीनतम खंड पढ़ना मुश्किल है, इसलिए आप इसे सरल बनाने के लिए अधिक कस्टम ब्लॉकों का उपयोग करने जा रहे हैं।

\--- task \--- `clear song`{:class="block3myblocks"} नामक एक और ब्लॉक बनाएँ जो दोनों सूचियों में से सभी आइटमों को हटा देता है। सूचियों में स्वरों को वापस जोड़ने से पहले इस ब्लॉक का उपयोग करें।

![note-sprite](images/note-sprite.png)

```blocks3
define clear song
delete (all v) of [notes v]
delete (all v) of [times v]
```

जब आप अपने कोड का परीक्षण करते हैं, तो उसे पहले की तरह ही काम करना चाहिए।

```blocks3
define load 'happy birthday'
+clear song ::custom
add [1] to [notes v]
add [5] to [notes v]
```

\--- /task \---

\--- task \--- आपका कोड और भी आसानी से पढ़ा जा सके, इसके लिए एक और ब्लॉक बनाएँ जिससे आप बजाए जाने वाले किसी स्वर और उसे बजाए जाने के समय को निर्दिष्ट कर सकें।

[[[generic-scratch3-make-block-parameters]]]

\--- hints \--- \--- hint \--- एक ब्लॉक बनाएँ जो किसी संख्या को `note`{:class="block3variables"} स्वर के रूप में लेता है और किसी संख्या को `time`{:class="block3variables"} समय के रूप में लेता है और सही संख्या को सही सूची में `adds`{:class="block3variables"} जोड़ता है। \--- /hint \--- \--- hint \--- यहाँ दिखाया गया है कि आपका कोड कैसा दिखना चाहिए:

```blocks3
define Add note (note) at (time) secs
add (note :: custom-arg) to [notes v]
add (time :: custom-arg) to [times v]

define load 'happy birthday'
clear song ::custom
+Add note (1) at (5) secs
+Add note (1) at (5.5) secs
+Add note (3) at (6) secs
+Add note (1) at (7) secs
+Add note (6) at (8) secs
+Add note (5) at (9) secs
```

\--- /hint \--- \--- /hints \---

\--- /task \---