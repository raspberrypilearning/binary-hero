## Key presses

How many notes can you play with four keys? It might be more than you think!

--- task ---
Open the starter project.

**Online:** Open the 'Binary Hero' Scratch starter project at [rpf.io/binary-hero-on](http://rpf.io/binary-hero-on){:target="_blank"}. You can click on 'Remix' in the top right-hand corner to save a copy of the project if you have a Scratch account.

**Offline:** Open the [starter project](http://rpf.io/p/binary-hero-go){:target="_blank"}in the offline editor. If you need to download the Scratch offline editor you will find it at [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.
--- /task ---

--- task ---
Let's start by showing which keys have been pressed. Click on the sprite called '1', and add code to change its costume when the `v` key is pressed.

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

When you test your sprite by pressing the `v` key, the sprite should light up.

![Testing the v key](images/1-test.png)
--- /task ---

--- task ---
Do the same for the other three sprites, so that they light up when the `c`, `x`, and `z` keys are pressed.

![All keys pressed](images/all-key-presses.png)
--- /task ---
