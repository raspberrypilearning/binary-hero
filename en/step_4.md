## Playing notes

Let's play notes when keys are pressed.

--- task ---
Broadcast a 'note change' message whenever *each of the four keys* is pressed.
![sprite 1](images/1.png)
```blocks
when flag clicked
forever
if < key [v v] pressed?> then
switch costume to [on v]
+broadcast [note change v]
else
switch costume to [off v]
end
```
--- /task ---

--- task ---
Add code to the Stage to play a note when a combination of keys is pressed.

Your notes should start at middle C, which is note 60.

![1 sprite](images/1.png)
```blocks
play note (60 v) for (1) beats
```

--- hints ---
--- hint ---
When your stage `receives`{:class="blockevents"} the 'change note' message, it should `stop all sounds`{:class="blocksound"} before `playing a note`{:class="blocksound"} based on the value of your `note`{:class="blockdata"} variable.

+ When your `note`{:class="blocksounds"} variable is `1`{:class="blockdata"}, note 60 should be played
+ When your `note`{:class="blocksounds"} variable is `2`{:class="blockdata"}, note 61 should be played
+ When your `note`{:class="blocksounds"} variable is `3`{:class="blockdata"}, note 62 should be played
+ etc...

--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![stage](images/stage.png)
```blocks
play note (60 v) for (1) beats
when I receive [note change v]
() + ()
(note)
stop all sounds
```
--- /hint ---
--- hint ---
This is what your code should look like:
![stage](images/stage.png)
```blocks
when I receive [note change v]
stop all sounds
play note ((59) + (note)) for (1) beats
```
--- /hint ---
--- /hints ---
--- /task ---

--- task ---
Test your code. You'll notice that the note is repeatedly played when a key is held down.
--- no-print ---
<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  Your browser does not support HTML5 video.
</video>
--- /no-print ---
--- /task ---

--- task ---
Can you add code so that the key sprites only play a note *once* when a key is held down?

--- hints ---
--- hint ---
When each of the `z`, `x`, `c` and `v` keys is pressed, your code should `wait until`{:class="blockcontrol"} the `key is not pressed`{:class="blocksensing"} before continuing.
--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![1 sprite](images/1.png)
```blocks
key [v v] pressed?
not <>
wait until <>
```
--- /hint ---
--- hint ---
This is what your code should look like:
![1 sprite](images/1.png)
```blocks
when flag clicked
forever
if < key [v v] pressed?> then
switch costume to [on v]
broadcast [note change v]
+wait until <not <key [v v] pressed?>
else
switch costume to [off v]
end
```
--- /hint ---
--- /hints ---
--- /task ---
