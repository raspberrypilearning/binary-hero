## अपना गाना संगृहीत करें

फिलहाल, स्वरों को बजाए जाने के बाद सूचियों से हटा दिया जाता है, इसलिए आपके पास खाली सूचियाँ बच जाती हैं:

![खाली सूचियाँ](images/empty-lists.png)

अब आप अपने प्रोजेक्ट में गाने संगृहीत करने के लिए कोड जोड़ने जा रहे हैं, ताकि आपको इन्हें अपनी सूचियों में हर बार न जोड़ना पड़े।

![सूचियों में स्वर और समय जोड़ें](images/lists-add-annotated.png)

\--- task \--- `load 'happy birthday'`{:class="block3myblocks"} नामक एक नया ब्लॉक बनाएँ जो `notes`{:class="block3variables"} और `times`{:class="block3variables"} दोनों सूचियों को साफ कर देता है, और फिर सही स्वरों को दोनों सूचियों में वापस जोड़ता है। [[[generic-scratch3-make-block]]] \--- hints \--- \--- hint \--- `load 'happy birthday'`{:class="block3myblocks"} ब्लॉक को `notes`{:class="block3variables"} और `times`{:class="block3variables"} दोनों सूचियों में से सभी आइटमों को `delete all`{:class="block3variables"} हटा देना चाहिए और फिर < 0>add</code>{:class="block3variables"} उन सही छह स्वरों को सही क्रम में उस सूची में जोड़ देना चाहिए जिस सूची में से वे हैं। \--- /hint \--- \--- hint \--- ये वे कोड ब्लॉक हैं जिनकी आपको आवश्यकता है: ![notes-sprite](images/note-sprite.png)

```blocks3
delete (all v) of [notes v]

define load 'happy birthday'

add [1] to [notes v]

delete (all v) of [times v]
```

\--- /hint \--- \--- hint \--- यहाँ दिखाया गया है कि आपका कोड कैसा दिखना चाहिए: ![notes-sprite](images/note-sprite.png)

```blocks3
define load 'happy birthday'
delete (all v) of [notes v]
delete (all v) of [times v]
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

\--- कार्य \--- अपने नए ब्लॉक को प्रोजेक्ट के प्रारंभ में चलाकर इसका परीक्षण करें। ![notes-sprite](images/note-sprite.png)

```blocks3
when flag clicked
+load 'happy birthday' ::custom
hide
reset timer
```

आपकी प्रत्येक सूची में अब छह स्वर होने चाहिए।

![स्वरों और समयों की सूची](images/lists-add.png) \--- /task \---