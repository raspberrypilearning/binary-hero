## स्वरों को स्क्रॉल करना

आपको स्वरों को स्टेज को नीचे स्क्रॉल करने की आवश्यकता है ताकि खिलाड़ी को पता चल सके कि कौन सी कुंजियों को दबाया जाए और उन्हें कब दबाया जाए।

\--- task \---

Create two lists called `notes`{:class="block3variables"} and `times`{:class="block3variables"}.

[[[generic-scratch3-make-list]]]

\--- /task \---

\--- task \---

Add the following numbers to your `notes`{:class="block3variables"} and `times`{:class="block3variables"} lists. Note: make sure to **add these exact numbers in the right order**.

![Add notes and times to lists](images/lists-add-annotated.png)

\--- /task \---

Here's how songs are stored in your game:

+ `notes`{:class="block3variables"} सूची में गाने के स्वरों को (1 से 15 तक), क्रम से संगृहीत किया जाता है।
+ `times`{:class="block3variables"} सूची में उन समयों को संगृहीत किया जाता है जब गाने में स्वरों को बजाया जाना चाहिए।

![Explaining lists](images/lists-explain.png)

So with the two new lists:

+ स्वर 1 (मध्य C) 5 सेकंड पर बजाया जाना चाहिए
+ स्वर 1 को 5.5 सेकंड पर दुबारा बजाया जाना चाहिए
+ स्वर 3 को 6 सेकंड पर बजाया जाना चाहिए
+ आदि...

\--- task \---

Click on the 'note' sprite and then click on **show**.

![Show the bar sprite](images/note-show-annotated.png)

Then click on **Costumes**.

![Bar sprite costumes](images/note-costumes.png)

\--- /task \---

You should see that the 'note' sprite has 15 different costume, one for each different note from 1 to 15.

\--- task \---

Add code to create a 'note' sprite clone for every note stored in `notes`{:class="block3variables"}. Each clone should be created at the correct time stored in `times`{:class="block3variables"}. Each clone should be created two seconds before its note needs to be played. This gives the clone two seconds to move down the screen. You'll create the code to move your clones in a little bit!

![Testing clones](images/clones-test.png)

\--- hints \--- \--- hint \---

![note](images/note-sprite.png) When the `flag is clicked`{:class="block3events"}, the 'note' sprite should `hide`{:class="block3looks"}, and the `timer`{:class="block3variables"} should be `reset`{:class="block3variables"}.

The script should then `wait until`{:class="block3control"} the value of `timer`{:class="block3variables"} is `greater than`{:class="block3operators"} the next note to be played, which will be the `time`{:class="block3variables"} at the `start of the list`{:class="block3variables"} (`minus 2 seconds`{:class="block3operators"}).

The costume for the 'note' sprite should then be set to the next `note`{:class="block3variables"} to be played (the `note`{:class="block3variables"} at the start of the list), before a `clone`{:class="block3events"} of the 'note' sprite is created.

The items at the start of the `notes`{:class="block3variables"} and `times`{:class="block3variables"} lists should then be `deleted`{:class="block3variables"}, and the entire process should be `repeated until`{:class="block3control"} there are no items left in the `notes`{:class="block3variables"} list.

\--- /hint \--- \--- hint \---

Here are the code blocks you need:

![note](images/note-sprite.png)

```blocks3
wait until <>
when flag clicked
length of [notes v]

create clone of (myself v)

reset timer
item (1 v) of [times v]
hide

repeat until <>
end
[] > []
item (1 v) of [notes v]
() - ()
switch costume to ( v)
[] = []
timer
delete (1 v) of [times v]

delete (1 v) of [notes v]
```

\--- /hint \--- \--- hint \---

This is what your code should look like:

![note](images/note-sprite.png)

```blocks3
when flag clicked
reset timer
hide
repeat until <(length of [notes v]) = [0]>
wait until <(timer) > ((item (1 v) of [times v]) - (2))>
switch costume to (item (1 v) of [notes v])
create clone of (myself v)
delete (1 v) of [times v]
delete (1 v) of [notes v]
end
```

\--- /hint \--- \--- /hints \--- \--- /task \---

When you test your code now, nothing seems to happen, because the 'note' sprite is hidden. If you show (or don't hide) the sprite, then you should see clones being created on top of each other.

\--- task \---

Add code to make each 'note' clone glide from the top to the bottom of the Stage before being deleted.

![note](images/note-sprite.png)

```blocks3
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
delete this clone
```

\--- /task \---