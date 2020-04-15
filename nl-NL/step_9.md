## Uitdaging: ga verder

Je spel is nu klaar, maar er zijn een paar dingen die je kunt doen om het nog beter te maken als je wilt!

Kun je bijvoorbeeld code toevoegen om het uiterlijk van het werkgebied te wijzigen als de juiste noot niet wordt gespeeld?

```blocks3
when I start as a clone
ga naar x: (20) y: (160)
verschijn
schuif in (2) sec. naar x: (20) y: (-130)
als <(noot :: variables) = (uiterlijk [nummer v])> dan
verander [score v] met (1)
zend signaal (correct v)
anders
+???
einde
verwijder deze kloon
```

Om dit te doen, moet je code toevoegen die erg lijkt op de code die de achtergrond verandert wanneer de juiste noot wordt gespeeld. Het project bevat nog een achtergrond die je kunt gebruiken.