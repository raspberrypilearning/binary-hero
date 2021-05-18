## नोट्स करना

जब चांबियाँ को दबाया जाए तो स्वर बजाएँ।

\--- task \---

अपने प्रोजेक्ट में संगीत विस्तार जोड़ें।

[[[generic-scratch3-add-music-extension]]]

\--- /task \---

\--- task \---

जब भी **चार कुंजियों में से किसी भी कुंजी **को दबाया जाता है तो 'स्वर परिवर्तन' का संदेश प्रसारित करें।

![स्प्राइट 1](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (on v)
+broadcast (note change v)
else
switch costume to (off v)
end
```

\--- /task \---

\--- task \---

चांबियाँ का संयोजन दबाए जाने पर किसी स्वर को बजाने के लिए स्टेज में कोड जोड़ें।

आपके स्वर मध्य C से शुरू होने चाहिए, जो स्वर 60 है।

```blocks3
play note (60) for (1) beats
```

\--- hints \--- \--- hint \---

![1 स्प्राइट](images/stage.png)

आपका स्टेज जब `receives`{:class="block3events"} ''स्वर बदलें' प्रसारण प्राप्त करता है, तो `note`{:class="block3variables"} वेरिएबल के मान के आधार पर `playing a note`{:class="block3sound"} से पहले इसे `stop all sounds`{:class="block3sound"} सभी ध्वनियों को बंद कर देना चाहिए।

+ जब `note`{:class="block3variables"} वेरिएबल `1`{:class="block3variables"} हो, तो स्वर 60 बजना चाहिए
+ जब `note`{:class="block3variables"} वेरिएबल `2`{:class="block3variables"} हो, तो स्वर 61 बजना चाहिए
+ जब `note`{:class="block3variables"} वेरिएबल `3`{:class="block3variables"} हो, तो स्वर 62 बजना चाहिए
+ आदि...

\--- /hint \--- \--- hint \---

आपको इस कोड ब्लॉक की ज़रुरत पड़ेगी:

![मंच](images/stage.png)

```blocks3
play note (60) for (1) beats
when I receive [note change v]
() + ()
(note)
stop all sounds
```

\--- /hint \--- \--- hint \---

आपका कोड ऐसा दिखना चाहिए:

![मंच](images/stage.png)

```blocks3
when I receive [note change v]
stop all sounds
play note ((59) + (note :: variables)) for (1) beats
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- task \---

अपने कोड का परीक्षण करें। क्या आप सुन सकते हैं कि जब आप किसी चाबी को दबाकर रखते हैं तो कोई स्वर बार-बार बजता है?

\--- no-print \---

<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  आपका ब्राउज़र HTML5 वीडियो का समर्थन नहीं करता है।
</video>

\--- /no-print \---

\--- /task \---

\--- task \---

Add code so that the **all** the key sprites only play a note **once** when a key is held down.

![1 स्प्राइट](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (on v)
broadcast (note change v)
+wait until <not <key (v v) pressed?>
else
switch costume to (off v)
end
```

\--- /task \---