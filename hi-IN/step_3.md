## बाइनरी संख्याएँ

आप विभिन्न स्वरों को बजाने के लिए चार कुंजियों को दबाने वाले विभिन्न संयोजनों का उपयोग करेंगे। प्रत्येक कुंजी या तो ऑन (दबाई गई) होती है या ऑफ (न दबाई गई) होती है। इसका मतलब है कि आप कुंजियों के प्रत्येक संयोजन को **binary number** (बाइनरी संख्या) के रूप में सोच सकते हैं।

दाएँ से बाएँ ओर चलते हुए कुंजियों का मूल्य दुगुना होता चला जाता है: `1`, `2`, `4`, और `8`। दबाई गई कुंजियों के ऊपर की संख्याओं को जोड़कर, आप स्वर के मान का पता लगा सकते हैं।

![स्वर मान के उदाहरण](images/note-values.png)

चारों कुंजियों को दबाने के 2<sup>4</sup> = **16 combinations** (संयोजन) हैं। इसका मतलब है कि आप 15 अलग-अलग स्वर बजा सकते हैं, क्योंकि `0` का मतलब होगा कि कोई स्वर नहीं बजता है।

--- task ---

`note`{:class="block3variables"}, और चार नोट स्प्राइट के बगल में खींचें।

![नोट चर](images/note-create.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

`note`{:class="block3variables"} उस नोट के मूल्य को संग्रहीत करेगा जिसे खेला जाना चाहिए।

--- task ---

मूल्य के गणना के लिए दबाए गए कुंजी के संयोजन का उपयोग करने के लिए स्टेज में ये कोड जोड़ें `note`{:class="block3variables"}.

उदाहरण के लिए, जब `c` तथा `v` दबाया जाता है, तो यह मूल्य {:class="block3variables"} should be `3`.

![नोट चर का परीक्षण](images/note-test.png)

--- hints ---
 --- hint ---

![मंच](images/stage.png)

जब `flag is clicked`{:class="block3events"} तब `note`{:class="block3variables"} अस्थायी क `set`{:class="block3variables"} to `0`{:class="block3variables"}.

+ `if`{:class="block3control"} the `v key is pressed`{:class="block3sensing"}, the `note`{:class="block3variables"} होना चाहिए `changed by 1`{:class="block3variables"}
+ `if`{:class="block3control"} the `c key is pressed`{:class="block3sensing"}, the `note`{:class="block3variables"} होना चाहिए `changed by 2`{:class="block3variables"}
+ `if`{:class="block3control"} the `x key is pressed`{:class="block3sensing"}, the `note`{:class="block3variables"} होना चाहिए `changed by 4`{:class="block3variables"}
+ `if`{:class="block3control"} the `z key is pressed`{:class="block3sensing"}, the `note`{:class="block3variables"} होना चाहिए `changed by 8`{:class="block3variables"}

ये सभी कोड को दोहराया जाना चाहिए `forever`{:class="block3control"}. 

--- /hint --- --- hint ---

यहां आपके लिए आवश्यक कोड ब्लॉक हैं, और आपको उनमें से कुछ को एक से अधिक बार जोड़ना होगा:

![मंच](images/stage.png)

```blocks3
forever
end
if < > then
end
key ( v) pressed?

change [note v] by ( )

set [note v] to [ ]

when flag clicked
```

--- /hint --- --- hint ---

यह वही है जो आपका कोड दिखना चाहिए:

![मंच](images/stage.png)

```blocks3
when flag clicked
forever
set [note v] to [0]
if <key (v v) pressed? > then
change [note v] by (1)
end
if <key (c v) pressed? > then
change [note v] by (2)
end
if <key (x v) pressed? > then
change [note v] by (4)
end
if <key (z v) pressed? > then
change [note v] by (8)
end
end
```

--- /hint ------ /hints --- --- /task ---