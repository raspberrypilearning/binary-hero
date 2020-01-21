## बाइनरी संख्याएँ

आप विभिन्न स्वरों को बजाने के लिए चार कुंजियों को दबाने वाले विभिन्न संयोजनों का उपयोग करेंगे। प्रत्येक कुंजी या तो ऑन (दबाई गई) होती है या ऑफ (न दबाई गई) होती है। इसका मतलब है कि आप कुंजियों के प्रत्येक संयोजन को **binary number** (बाइनरी संख्या) के रूप में सोच सकते हैं।

दाएँ से बाएँ ओर चलते हुए कुंजियों का मूल्य दुगुना होता चला जाता है: `1`, `2`, `4`, और `8`। दबाई गई कुंजियों के ऊपर की संख्याओं को जोड़कर, आप स्वर के मान का पता लगा सकते हैं।

![स्वर मान के उदाहरण](images/note-values.png)

चारों कुंजियों को दबाने के 2<sup>4</sup> = **16 combinations** (संयोजन) हैं। इसका मतलब है कि आप 15 अलग-अलग स्वर बजा सकते हैं, क्योंकि `0` का मतलब होगा कि कोई स्वर नहीं बजता है।

\--- task \---

Create a new variable called `note`{:class="block3variables"}, and drag it next to the four note sprites.

![Note variable](images/note-create.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

`note`{:class="block3variables"} will store the value of the note that should be played.

\--- task \---

Add code to the Stage to use the combination of pressed keys to calculate the value of `note`{:class="block3variables"}.

For example, when `c` and `v` are pressed, the value of `note`{:class="block3variables"} should be `3`.

![Testing the note variable](images/note-test.png)

\--- hints \--- \--- hint \---

![stage](images/stage.png)

When the `flag is clicked`{:class="block3events"}, the `note`{:class="block3variables"} variable should be `set`{:class="block3variables"} to `0`{:class="block3variables"}.

+ `if`{:class="block3control"} the `v key is pressed`{:class="block3sensing"}, the `note`{:class="block3variables"} should be `changed by 1`{:class="block3variables"}
+ `if`{:class="block3control"} the `c key is pressed`{:class="block3sensing"}, the `note`{:class="block3variables"} should be `changed by 2`{:class="block3variables"}
+ `if`{:class="block3control"} the `x key is pressed`{:class="block3sensing"}, the `note`{:class="block3variables"} should be `changed by 4`{:class="block3variables"}
+ `if`{:class="block3control"} the `z key is pressed`{:class="block3sensing"}, the `note`{:class="block3variables"} should be `changed by 8`{:class="block3variables"}

All of this code should be repeated `forever`{:class="block3control"}.

\--- /hint \--- \--- hint \---

Here are the code blocks you need, and you have to add some of them more than once:

![stage](images/stage.png)

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

\--- /hint \--- \--- hint \---

This is what your code should look like:

![stage](images/stage.png)

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

\--- /hint \--- \--- /hints \--- \--- /task \---