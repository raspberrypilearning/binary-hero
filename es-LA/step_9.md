## Desafío: ve más allá

¡Tu juego ya está hecho, pero si quieres, hay algunas cosas que puedes hacer para hacerlo aún mejor!

Por ejemplo, ¿puedes agregar código para cambiar la apariencia del Escenario si no se toca la nota correcta?

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

Para hacer esto, necesitas agregar código que sea muy similar al código que cambia el fondo cuando se toca la nota correcta. El proyecto contiene otro fondo que puedes usar.