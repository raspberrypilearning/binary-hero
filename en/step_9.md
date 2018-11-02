## Challenge: taking it further

Your Binary Hero game is done now, but there are a few things you could do to make it even better!

For example, can you add code to change how the stage looks if the correct note isn't played?

```blocks
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
if <(note) = (costume #)> then
change [score v] by (1)
broadcast [correct v]
else
+???
end
delete this clone
```

You'll need to add code very similar to the code for when a correct note is played, and a costume has been provided for you.
