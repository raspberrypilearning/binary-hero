## Binary notes

How many notes can you play with 4 keys? It might be more than you think!

+ Open the starter project.

--- collapse ---
---
title: I'm using Scratch online
image: images/image.png
---
Open the 'Binary Hero' Scratch starter project at  [http://jumpto.cc/binary-go"](jumpto.cc/binary-go){:target="_blank"}.
--- /collapse ---

--- collapse ---
---
title: I'm using Scratch offline
image: images/image.png
---
Download the 'Binary Hero' Scratch starter project from [resources/binary-hero](resources/binary-hero){:target="_blank"} and then open it using the offline editor.
--- /collapse ---

+ Binary intro???

+ Let's start by showing which keys have been pressed. Click on the sprite called '1' and add code to change its costume when the v key is pressed.

When you test your sprite by pressing the v key, the sprite should light up.

![Testing the v key](images/1-test.png)

--- hints ---
--- hint ---
When the __flag is clicked__, your sprite should check __forever__ whether the __v key is pressed__. __If__ the key is pressed the 'on' __costume__ should be shown, __else__ the 'off' __costume__ should be shown.
--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![Blocks for changing costumes](images/key-press-blocks.png)
--- /hint ---
--- hint ---
This is what your code should look like:
![Code for changing costumes](images/key-press-code.png)
--- /hint ---
--- /hints ---

[[[generic-scratch-saving]]]

+ Do the same for the other 3 sprites, so that they light up when the c, x and z key are pressed.

+ Create a new variable called `note`, and drag it next to the 4 note sprites.

![Note variable](images/note-create.png)

[[[generic-scratch-add-variable]]]

+ Add code to the **stage** to used the keys pressed to calculate the value of the note to be played.

--- hints ---
--- hint ---
When the __flag is clicked__, the `note` variable should be __set__ to `0`.

+ __If__ the v __key is pressed__, the `note` should be __changed by 1__.
+ __If__ the c __key is pressed__, the `note` should be __changed by 2__.
+ __If__ the x __key is pressed__, the `note` should be __changed by 4__.
+ __If__ the z __key is pressed__, the `note` should be __changed by 8__.

All of this code should be repeated __forever__.
--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![Blocks for calculating the note](images/calculate-note-blocks.png)
--- /hint ---
--- hint ---
This is what your code should look like:
![Code for calculating the note](images/calculate-note-code.png)
--- /hint ---
--- /hints ---
