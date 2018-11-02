## Keeping score

Improve your game by giving the player points each time the correct note is played.

--- task ---
Create a new variable called `score`{:class="blockdata"}, and place it at the top of your stage.

![Add a score](images/add-score.png)
--- /task ---

--- task ---
Add to the player's score whenever they play the correct note at the correct time. Remember to set their score to `0` at the start of the game.

--- hints ---
--- hint ---
`Before each clone is deleted`{:class="blockcontrol"}, it should check to see `if`{:class="blockcontrol"} the `note`{:class="blockdata"} is `equal to`{:class="blockoperators"} the `costume number`{:class="blocklooks"}. If they are the same, the score can be `changed`{:class="blockdata"}.
--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![note](images/note-sprite.png)
```blocks
[ ] = [ ]
(costume #)
(note)
change [score v] by (1)

if <> then
else
end
```
--- /hint ---
--- hint ---
This is what your code should look like:
![note](images/note-sprite.png)
```blocks
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
+if <(note) = (costume #)> then
change [score v] by (1)
else
end
delete this clone
```
--- /hint ---
--- /hints ---
--- /task ---

--- task ---
Broadcast a message called 'correct' when the correct note is played.
![note](images/note-sprite.png)
```blocks
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
if <(note) = (costume #)> then
change [score v] by (1)
+broadcast [correct v]
else
end
delete this clone
```
--- /task ---

--- task ---
Add code to your Stage to briefly change how it looks when the player plays the correct note. A costume has been provided for you.

![Correct stage background](images/correct-costume.png)

![stage](images/stage.png)
```blocks
when flag clicked
switch backdrop to [normal v]

when I receive [correct v]
switch backdrop to [correct v]
wait (0.3) secs
switch backdrop to [normal v]
```
--- /task ---
