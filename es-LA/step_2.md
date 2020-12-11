## Presionar teclas

¿Cuántas notas puedes tocar con cuatro teclas? ¡Podrían ser más de las que piensas!

\--- task \---

Open the 'Binary hero' Scratch starter project.

**Online:** open the starter project at [rpf.io/binary-hero-on](http://rpf.io/binary-hero-on){:target="_blank"}. Si tienes una cuenta de Scratch, puedes guardar una copia del proyecto al hacer clic en **Remix**, en la esquina superior derecha.

**Sin conexión**: abre el [proyecto inicial](http://rpf.io/p/en/binary-hero-go){:target=_blank"} en el editor sin conexión. Si necesitas descargar e instalar el editor sin conexión de Scratch, puedes encontrarlo en [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

Start by showing which key is being pressed.

\--- task \---

Click on the sprite called '1', and add code to change the sprite's costume if the `v` key is pressed.

![disfraz](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (on v)
else
switch costume to (off v)
end
```

Cuando pruebas tu código al presionar la tecla <kbd>v</kbd>, el objeto se debería encender.

![Probando la tecla v](images/1-test.png)

\--- /task \---

\--- task \---

Haz lo mismo con los otros tres objetos para que se enciendan al presionar las teclas <kbd>z</kbd>, <kbd>x</kbd>, o <kbd>c</kbd>.

![Todas las teclas presionadas](images/all-key-presses.png)

\--- /task \---