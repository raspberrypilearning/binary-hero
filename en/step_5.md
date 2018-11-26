## Scrolling notes

Scroll notes down the stage so that the player knows which keys to press.

--- task ---
Create two lists called `notes`{:class="blockdata"} and `times`{:class="blockdata"}.

[[[generic-scratch-make-list]]]
--- /task ---

--- task ---
Add the following numbers to your `notes`{:class="blockdata"} and `times`{:class="blockdata"} lists. Note: make sure to add these exact numbers in the right order.

![Add notes and times to lists](images/lists-add.png)
--- /task ---

Here's how songs will be stored:

+ The `notes`{:class="blockdata"} list stores the notes of the song, in order (from 1 to 15).
+ The `times`{:class="blockdata"} list is used to store the times that each note is played.

![Explaining lists](images/lists-explain.png)

So for the data above:

+ Note 1 (middle C) should be played at 5 seconds
+ Note 1 should be played again at 5.5 seconds
+ Note 3 should be played at 6 seconds
+ etc...

--- task ---
Right-click on the 'note' sprite and click **show**.

![Show the bar sprite](images/note-show.png)

Click **Costumes**, you should see that the sprite has 15 different costume, one for each note.

![Bar sprite costumes](images/note-costumes.png)
--- /task ---

--- task ---
Add code to create a clone of the 'note' sprite for every note to be played. Each clone should be created two seconds before the time the note should be played, and should then move down the stage.

This will give the clone two seconds to move down the screen. You'll create the code to move your clones in a little bit!

Nothing will seem to happen when you test your code, because the 'note' sprite is hidden. If you show (or don't hide) the sprite, then you should see clones being created on top of each other.

![Testing clones](images/clones-test.png)

--- hints ---
--- hint ---
![note](images/note-sprite.png)
When the `flag is clicked`{:class="blockevents"} the 'note' sprite should `hide`{:class="blocklooks"}, and the `timer`{:class="blockdata"} should be `reset`{:class="blockdata"}.

You should then `wait until`{:class="blockcontrol"} the timer is `greater than`{:class="blockoperators"} the next note to be played, which will be the `time`{:class="blockdata"} at the `start of the list`{:class="blockdata"} (`minus 2 seconds`{:class="blockoperators"}).

The costume for the 'note' sprite should then be set to the next `note`{:class="blockdata"} to be played (the `note`{:class="blockdata"} at the start of the list), before a `clone`{:class="blockevents"} of the note sprite is created.

The items at the start of the `notes`{:class="blockdata"} and `times`{:class="blockdata"} lists can then be `deleted`{:class="blockdata"}, and the entire process should be `repeated until`{:class="blockcontrol"} there are no notes left.

--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![note](images/note-sprite.png)
```blocks
wait until <>
when flag clicked
length of [notes v]

create clone of [myself v]

reset timer
item (1 v) of [times v]
hide

repeat until <>
end
[] > []
item (1 v) of [notes v]
() - ()
switch costume to [ v]
[] = []
timer
delete (1 v) of [times v]

delete (1 v) of [notes v]
```

--- /hint ---
--- hint ---
This is what your code should look like:
![note](images/note-sprite.png)
```blocks
when flag clicked
reset timer
hide
repeat until <(length of [notes v]) = [0]>
wait until <(timer) > ((item (1 v) of [times v]) - (2))>
switch costume to (item (1 v) of [notes v])
create clone of [myself v]
delete (1 v) of [times v]
delete (1 v) of [notes v]
end
```
--- /hint ---
--- /hints ---
--- /task ---

--- task ---
Now add code to make each note clone glide from the top to the bottom of the screen before being deleted.
![note](images/note-sprite.png)
```blocks
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
delete this clone
```
--- /task ---
