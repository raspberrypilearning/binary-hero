## Key presses

How many notes can you play with four keys? It might be more than you think!

--- task ---
Open the starter project.

**Online:** Open the 'Binary Hero' Scratch starter project at [rpf.io/binary-hero-on](http://rpf.io/binary-hero-on){:target="_blank"}. You can click on 'Remix' in the top right-hand corner to save a copy of the project if you have a Scratch account.

**Offline:** Open the [starter project](resources/binary-hero.sb2) in the offline editor. If you need to download the Scratch offline editor you will find it at [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.
--- /task ---

--- task ---
Let's start by showing which keys have been pressed. Click on the sprite called '1', and add code to change its costume when the `v` key is pressed.

When you test your sprite by pressing the `v` key, the sprite should light up.

![Testing the v key](images/1-test.png)

--- hints ---
--- hint ---
When the `flag is clicked`{:class="blockevents"}, your sprite should check `forever`{:class="blockcontrol"} whether the `v key is pressed`{:class="blocksensing"}. `if`{:class="blockcontrol"} the key is pressed, the 'on' `costume`{:class="blocklooks"} should be shown, `else`{:class="blockcontrol"} the 'off' `costume`{:class="blocklooks"} should be shown.
--- /hint ---
--- hint ---
Here are the code blocks you'll need:
![costume](images/1.png)
```blocks
switch costume to [on v]
when flag clicked
key [v v] pressed?
switch costume to [off v]

if < > then
else
end

forever
end
```
--- /hint ---
--- hint ---
This is what your code should look like:
![costume](images/1.png)
```blocks
when flag clicked
forever
if < key [v v] pressed?> then
switch costume to [on v]
else
switch costume to [off v]
end
```
--- /hint ---
--- /hints ---
--- /task ---

--- task ---
Do the same for the other three sprites, so that they light up when the `c`, `x`, and `z` keys are pressed.

![All keys pressed](images/all-key-presses.png)
--- /task ---
