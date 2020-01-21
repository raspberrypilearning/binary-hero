## स्वर बजाएँ

जब कुंजियों को दबाया जाए तो स्वर बजाएँ।

\--- task \---

अपने प्रोजेक्ट में Music एक्सटेंशन जोड़ें।

[[[generic-scratch3-add-music-extension]]]

\--- /task \---

\--- task \---

Broadcast a 'note change' message whenever **any of the four keys** is pressed.

![sprite 1](images/1.png)

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

Add code to the Stage to play a note when a combination of keys is pressed.

Your notes should start at middle C, which is note 60.

```blocks3
play note (60) for (1) beats
```

\--- hints \--- \--- hint \---

![1 sprite](images/stage.png)

When your stage `receives`{:class="block3events"} the 'change note' broadcast, it should `stop all sounds`{:class="block3sound"} before `playing a note`{:class="block3sound"} based on the value of the`note`{:class="block3variables"} variable.

+ जब `note`{:class="block3variables"} वेरिएबल `1`{:class="block3variables"} हो, तो स्वर 60 बजना चाहिए
+ जब `note`{:class="block3variables"} वेरिएबल `2`{:class="block3variables"} हो, तो स्वर 61 बजना चाहिए
+ जब `note`{:class="block3variables"} वेरिएबल `3`{:class="block3variables"} हो, तो स्वर 62 बजना चाहिए
+ आदि...

\--- /hint \--- \--- hint \---

Here are the code blocks you need:

![stage](images/stage.png)

```blocks3
play note (60) for (1) beats
when I receive [note change v]
() + ()
(note)
stop all sounds
```

\--- /hint \--- \--- hint \---

This is what your code should look like:

![stage](images/stage.png)

```blocks3
when I receive [note change v]
stop all sounds
play note ((59) + (note :: variables)) for (1) beats
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- task \---

Test your code. Can you hear that a note is repeatedly played when you hold down a key?

\--- no-print \---

<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  आपका ब्राउज़र HTML5 वीडियो का समर्थन नहीं करता है।
</video>

\--- /no-print \---

\--- /task \---

\--- task \---

Add code so that the **all** the key sprites only play a note **once** when a key is held down?

![1 sprite](images/1.png)

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