## Keeping score

Improve your game by giving the player points each time the correct note is played.

+ Create a new variable called `score`, and place it at the top of your stage.

![Add a score](images/add-score.png)

+ Add to the player's score whenever they play the correct note at the correct time. Remember to set their score to `0` at the start of the game.

--- hints ---
--- hint ---
__Before each clone is deleted__, it should check to see __if__ the __note__ is __equal to__ the __costume number__. If they are the same, the score can be __changed__.
--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![Blocks for keeping score](images/score-blocks.png)
--- /hint ---
--- hint ---
This is what your code should look like:
![Code for keeping score](images/score-code.png)
--- /hint ---
--- /hints ---

+ Broadcast a message called 'correct' when the correct note is played.

![Broadcasting a 'correct' message](images/broadcast-correct.png)

+ Add code to your **stage** to briefly change how it looks when the player plays the correct note.

--- hints ---
--- hint ---
When your stage __receives__ the 'correct' message, it should __switch costume__, __wait__ for a short time before __switching back__.

You might also need to add code to __set the costume__ to normal when the __flag is clicked__.
--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![Blocks for playing the correct note](images/stage-correct-blocks.png)
--- /hint ---
--- hint ---
This is what your code should look like:
![Code for playing the correct note](images/stage-correct-code.png)
--- /hint ---
--- /hints ---
