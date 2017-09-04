## Storing songs

You've made it so that notes are removed from the lists once they've been played, so you'll be left with empty lists:

![Empty lists](images/empty-lists.png)

You're now going to add code to store songs in your project, so that you don't have to add to your lists each time.

+ Make a block called `load 'happy birthday'` that clears both the `notes` and `times` lists, and then adds the numbers back into both lists.

Test your new block by running it at the start of your project.

![Testing a custom block](images/load-block-test.png)

Each of your lists should now contain five numbers.

![Lists of notes and times](images/load-list-test.png)

[[[generic-scratch-make-block]]]

--- hints ---
--- hint ---
When your new block is run, `all items` should be deleted from both the `notes` and `times` lists. Each of the five numbers should then be `added` to both lists.
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
Make a block called 'clear song' that `deletes` all items from both lists.
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
Make a block that takes a `note` and a `time` and `adds` both numbers to the lists.
--- /hint ---
--- hint ---
This is what your code should look like:
![screenshot](images/custom-note-code.png)
--- /hint ---
--- /hints ---
