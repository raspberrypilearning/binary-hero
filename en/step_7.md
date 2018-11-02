## More custom blocks

The code in the last step is difficult to read, so let's use more custom blocks to simplify it.

--- task ---
 Make another block called `clear song`, which deletes all items from both lists. Use this block before adding to the lists.

![note-sprite](images/note-sprite.png)
```blocks
define clear song
delete (all v) of [notes v]
delete (all v) of [times v]
```

When you test your code, it should work just as it did before.

```blocks
define load 'happy birthday'
+clear song ::custom
add [1] to [notes v]
add [5] to [notes v]
```
--- task ---
You could make your code even easier to read by making another block which allows you to specify a note to be played along with a time.

[[[generic-scratch-make-block-parameters]]]

--- hints ---
--- hint ---
Make a block that takes a `note`{:class="blockdata"} and a `time`{:class="blockdata"} and `adds`{:class="blockdata"} both numbers to the lists.
--- /hint ---
--- hint ---
This is what your code should look like:
```blocks
define Add note (note) at (time) secs
add (note) to [notes v]
add (time) to [times v]

define load 'happy birthday'
clear song ::custom
+Add note (1) at (5) secs
+Add note (1) at (5.5) secs
+Add note (3) at (6) secs
+Add note (1) at (7) secs
+Add note (6) at (8) secs
+Add note (5) at (9) secs
```
--- /hint ---
--- /hints ---

