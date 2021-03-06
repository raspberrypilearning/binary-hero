## Speel noten

Speel noten wanneer de toetsen worden ingedrukt.

--- task ---

Voeg de Muziek-uitbreiding toe aan je project.

[[[generic-scratch3-add-music-extension]]]

--- /task ---

--- task ---

Zend een bericht 'noot veranderen' uit wanneer **een van de vier toetsen** wordt gedrukt.

![sprite 1](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (aan v)
+broadcast (noot veranderen v)
else
switch costume to (uit v)
end
```

--- /task ---

--- task ---

Voeg code toe aan het speelveld om een noot te spelen wanneer een combinatie van toetsen wordt ingedrukt.

Je noten moeten beginnen bij middelste C, dat is noot 60.

```blocks3
speel noot (60) gedurende (1) maten
```

--- hints ---
 --- hint ---

![1 sprite](images/stage.png)

Als het `speeldveld`{:class="block3events"} het signaal 'noot veranderen' ontvangt, moet deze `alle geluiden stoppen`{:class="block3sound"} voordat `een noot`{:class="block3sound"} gespeeld wordt gebaseerd op de waarde van de variabele `noot`{:class="block3variables"}.

+ Als de variabele `noot`{:class="block3variables"} `1`{:class="block3variables"} is, moet noot 60 spelen
+ Als de variabele `noot`{:class="block3variables"} `2`{:class="block3variables"} is, moet noot 61 spelen
+ Als de variabele `noot`{:class="block3variables"} `3`{:class="block3variables"} is, moet noot 62 worden gespeeld
+ enz...

--- /hint --- --- hint ---

Dit zijn de codeblokken die je nodig hebt:

![speelveld](images/stage.png)

```blocks3
speel noot (60) gedurende (1) maten
wanneer ik signaal [noot veranderen v] ontvang
() + ()
(noot)
stop alle geluiden
```

--- /hint --- --- hint ---

Dit is hoe je code eruit zou moeten zien:

![speelveld](images/stage.png)

```blocks3
wanneer ik signaal [noot veranderen v] ontvang
stop alle geluiden
speel noot ((59) + (noot :: variables)) gedurende (1) maten
```

--- /hint ------ /hints --- --- /task ---

--- task ---

Test je code. Hoor je dat een noot herhaaldelijk wordt gespeeld als je een toets ingedrukt houdt?

--- no-print ---

<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  Je browser ondersteunt geen HTML5 video.
</video>

--- /no-print ---

--- /task ---

--- task ---

Voeg code toe zodat **alle** toets sprites een noot slechts **eenmaal** spelen als een toets continu wordt ingedrukt?

![1 sprite](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (aan v)
broadcast (noot veranderen v)
+wait until <not <key (v v) pressed?>
else
switch costume to (uit v)
end
```

--- /task ---