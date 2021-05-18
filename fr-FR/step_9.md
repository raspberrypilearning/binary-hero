## Défi : Aller plus loin

Ton jeu est maintenant terminé, mais il y a des choses que tu peux faire pour le rendre encore meilleur si tu le veux !

Par exemple, peux-tu ajouter du code pour changer l'apparence de la scène si la bonne note n'est pas jouée ?

```blocks3
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
if <(note :: variables) = (costume [number v])> then
change [score v] by (1)
broadcast (correct v)
else
+???
end
delete this clone
```

Pour faire çà, tu dois ajouter du code qui est très similaire au code qui change l'arrière-plan lorsque la bonne note est jouée. Le projet contient un autre arrière-plan que tu peux utiliser.