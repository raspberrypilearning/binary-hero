## स्कोर रखिए

सही स्वर बजाने के लिए खिलाड़ी को अंक देकर अपने गेम में सुधार करें।

--- task ---

नामक एक नया वेरिएबल बनाएँ `score`{:class="block3variables"},और इसे अपने स्टेज के शीर्ष पर रखें।

![एक अंक जोड़ें](images/add-score.png)

--- /task ---

--- task ---

जब भी खिलाड़ी सही समय पर सही स्वर बजाता है तो `score`{:class="block3variables"} स्कोर में जोड़ें। गेम के आरंभ में `score`{:class="block3variables"} को `0`{:class="block3variables"} पर सेट करना याद रखें।

--- hints ---
 --- hint ---

`Before each clone is deleted`{:class="block3control"}, इसे यह देखने के लिए जाँच करनी चाहिए कि `if`{:class="block3control"} यदि स्वर `note`{:class="block3variables"} परिधान की `equal to`{:class="block3operators"} संख्या के समान है `costume number`{:class="block3looks"}, तो उस स्थिति में, स्कोर को `changed`{:class="block3variables"} बदल दिया जाना चाहिए।

--- /hint --- --- hint ---

आपको इस कोड ब्लॉक की ज़रुरत पड़ेगी:

![टिप्पणी](images/note-sprite.png)

```blocks3
[ ] = [ ]
(costume [number v])
(note)
change [score v] by (1)

if <> then
else
end
```

--- /hint --- --- hint ---

आपका कोड ऐसा दिखना चाहिए:

![टिप्पणी](images/note-sprite.png)

```blocks3
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
+if <(note :: variables) = (costume [number v])> then
change [score v] by (1)
end
delete this clone
```

--- /hint ------ /hints --- --- /task ---

--- task ---

सही स्वर बजाए जाने पर 'correct' नामक संदेश प्रसारित करें।

![टिप्पणी](images/note-sprite.png)

```blocks3
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
if <(note :: variables) = (costume [number v])> then
change [score v] by (1)
+broadcast (correct v)
end
delete this clone
```

--- /task ---

--- task ---

![सही स्टेज बैकग्राउंड](images/correct-costume.png)

खिलाड़ी जब सही स्वर बजाए तो थोड़े समय के लिए पृष्ठभूमि को बदलने के लिए अपने स्टेज में कोड जोड़ें। इस प्रोजेक्ट में इसके लिए पहले से ही एक दूसरी पृष्ठभूमि शामिल है।

![मंच](images/stage.png)

```blocks3
when flag clicked
switch backdrop to (normal v)

when I receive [correct v]
switch backdrop to (correct v)
wait (0.3) seconds
switch backdrop to (normal v)
```

--- /task ---