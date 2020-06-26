## अधिक कस्टम ब्लॉक्स

कोड का नवीनतम खंड पढ़ना मुश्किल है, इसलिए आप इसे सरल बनाने के लिए अधिक कस्टम ब्लॉकों का उपयोग करने जा रहे हैं।

\--- task \---

एक अन्य ब्लॉक बनाएं जिसे `clear song`{:class="block3myblocks"} कहा जाता है जो दोनों सूची के सभी आइटमों को हटा देता है। संख्याओं को वापस जोड़ने से पहले इस ब्लॉक का उपयोग करें।

![नोट स्प्राइट](images/note-sprite.png)

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

\--- task \---

ताकि आपका कोड पढ़ना और भी आसान हो जाए, एक और ब्लॉक बनाएं जो आपको नोट किए जाने के लिए नोट करने की अनुमति दे और एक नोट को खेलने के लिए समय दे।

[[[generic-scratch3-make-block-parameters]]]

\--- hints \--- \--- hint \---

एक ऐसा ब्लॉक बनाएं जो एक संख्या को `note`{:class="block3variables"} और एक संख्या के रूप में `time`{:class="block3variables"} और `adds`{:class="block3variables"} प्रत्येक नंबर को सही सूची में।

\--- /hint \--- \--- hint \---

यह वही है जो आपका कोड दिखना चाहिए:

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