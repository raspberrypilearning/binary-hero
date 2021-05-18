## अपना गाना इकट्ठा करें

फिलहाल, स्वरों को बजाए जाने के बाद सूचियों से हटा दिया जाता है, इसलिए आपके पास खाली सूचियाँ बच जाती हैं:

![खाली सूचियाँ](images/empty-lists.png)

अब आप अपने प्रोजेक्ट में गाने संगृहीत करने के लिए कोड जोड़ने जा रहे हैं, ताकि आपको इन्हें अपनी सूचियों में हर बार न जोड़ना पड़े।

![सूचियों में स्वर और समय जोड़ें](images/lists-add-annotated.png)

\--- task \---

नामक एक नया ब्लॉक बनाएँ जो `load 'happy birthday'`{:class="block3myblocks"}दोनों सूचियों को साफ कर देता है`notes`{:class="block3variables"} और `times`{:class="block3variables"} सूचियों, और फिर सही स्वरों को दोनों सूचियों में वापस जोड़ता है। [[[generic-scratch3-make-block]]]

\--- hints \--- \--- hint \---

यह `load 'happy birthday'`{:class="block3myblocks"} ब्लॉक को `notes`{:class="block3variables"} और `times`{:class="block3variables"} दोनों सूचियों में से सभी आइटमों को `delete all`{:class="block3variables"} और फिर < 0>add</code>{:class="block3variables"} उन सही छह स्वरों को सही क्रम में उस सूची में जोड़ देना चाहिए जिस सूची में से वे हैं।

\--- /hint \--- \--- hint \---

आपको इन कोड ब्लॉक्स की ज़रुरत पड़ेगी:

![टिप्पणियाँ-स्प्राइट](images/note-sprite.png)

```blocks3
delete all of [notes v]

define load 'happy birthday'

add [1] to [notes v]

delete all of [times v]
```

\--- /hint \--- \--- hint \---

आपका कोड ऐसा दिखना चाहिए:

![टिप्पणियाँ-स्प्राइट](images/note-sprite.png)

```blocks3
define load 'happy birthday'
delete all of [notes v]
delete all of [times v]
add [1] to [notes v]
add [5] to [times v]
add [1] to [notes v]
add [5.5] to [times v]
add [3] to [notes v]
add [6] to [times v]
add [1] to [notes v]
add [7] to [times v]
add [6] to [notes v]
add [8] to [times v]
add [5] to [notes v]
add [9] to [times v]
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- task \---

अपने नए ब्लॉक को प्रोजेक्ट के प्रारंभ में चलाकर इसका परीक्षण करें।

![टिप्पणियाँ-स्प्राइट](images/note-sprite.png)

```blocks3
when flag clicked
+load 'happy birthday' ::custom
hide
reset timer
```

आपकी प्रत्येक सूची में अब छह स्वर होने चाहिए।

![स्वरों और समयों की सूची](images/lists-add.png)

\--- /task \---