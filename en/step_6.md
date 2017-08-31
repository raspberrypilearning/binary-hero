## Storing songs

+ Notes are removed from the lists once they've been played, so you're left with empty lists.

![Empty lists](images/empty-lists.png)

You're now going to add code to store songs in your project, so that you don't have to add to your lists each time.

+ Make a block called `load 'happy birthday'` that clears both lists and then adds the numbers back into both `notes` and `times` lists.

Test your new block by running it at the start of your project.

![Testing a custom block](images/load-block-test.png)

Your lists should now each contain 5 numbers.

![Lists of notes and times](images/load-list-test.png)

[[[generic-scratch-make-block]]]

--- hints ---
--- hint ---
When your new block is run, __all items__ should be deleted from both `notes` and `times` lists. Each of the 5 numbers should then be __added__ to both lists.
--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![screenshot](images/load-blocks.png)
--- /hint ---
--- hint ---
This is what your code should look like:
![screenshot](images/load-code.png)
--- /hint ---
--- /hints ---

+ The code above is difficult to read. Make another block called `clear song`, which deletes all items from both lists. Use this block before adding to the lists.

![Block to clear lists](images/clear-song-test.png)

When you test your code, it should work just as it did before.

--- hints ---
--- hint ---
Make a block called 'clear song' that __deletes__ all items from both lists.
--- /hint ---
--- hint ---
This is what your code should look like:
![screenshot](images/clear-song-code.png)
--- /hint ---
--- /hints ---

+ You could make your code even easier to read by making another block which allows you to specify a note to be played along with a time.

![Custom block for adding a note](images/custom-note-test.png)

When you test your code, it should work just as it did before.

[[[generic-scratch-make-block-parameters]]]

--- hints ---
--- hint ---
Make a block that takes a `note` and a `time` and __adds__ both numbers to the lists.
--- /hint ---
--- hint ---
This is what your code should look like:
![screenshot](images/custom-note-code.png)
--- /hint ---
--- /hints ---
