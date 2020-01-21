## Liczby binarne

Użyjesz różnych kombinacji naciskania czterech klawiszy, aby grać różne nuty. Każdy z klawiszy jest włączony (wciśnięty) lub wyłączony (nie wciśnięty). Oznacza to, że każdą kombinację kluczy można traktować jako liczbę binarną ****.

Przechodzenie z prawej do lewej klawisze mają podwójną wartość: `1`, `2`, `4`i `8`. Dodając liczby powyżej naciśniętych klawiszy, możesz obliczyć wartość nuty.

![Zwróć uwagę na przykłady wartości](images/note-values.png)

Istnieją 2<sup>4</sup> = **16 kombinacji** naciśnięcia czterech klawiszy. Oznacza to, że możesz grać 15 różnych dźwięków, ponieważ `0` oznacza, że żadna nuta nie jest odtwarzana.

\--- task \---

Create a new variable called `note`{:class="block3variables"}, and drag it next to the four note sprites.

![Note variable](images/note-create.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

`note`{:class="block3variables"} will store the value of the note that should be played.

\--- task \---

Add code to the Stage to use the combination of pressed keys to calculate the value of `note`{:class="block3variables"}.

For example, when `c` and `v` are pressed, the value of `note`{:class="block3variables"} should be `3`.

![Testing the note variable](images/note-test.png)

\--- hints \--- \--- hint \---

![stage](images/stage.png)

When the `flag is clicked`{:class="block3events"}, the `note`{:class="block3variables"} variable should be `set`{:class="block3variables"} to `0`{:class="block3variables"}.

+ `jeśli`{: class = "block3control"} naciśniesz klawisz `v`{: class = "block3sensing"}, `nutę`{: class = "block3variables"} należy zmienić o `o 1`{: class = „block3variables”}
+ `jeśli`{: class = "block3control"} naciśniesz klawisz `c`{: class = "block3sensing"}, `nutę`{: class = "block3variables"} należy zmienić o `o 2`{: class = „block3variables”}
+ `jeśli`{: class = "block3control"} naciśniesz klawisz `x`{: class = "block3sensing"}, `nutę`{: class = "block3variables"} należy zmienić `o 4`{: class = „block3variables”}
+ `jeśli`{: class = "block3control"} naciśniesz klawisz `z`{: class = "block3sensing"}, `nutę`{: class = "block3variables"} należy zmienić `o 8`{: class = „block3variables”}

All of this code should be repeated `forever`{:class="block3control"}.

\--- /hint \--- \--- hint \---

Here are the code blocks you need, and you have to add some of them more than once:

![stage](images/stage.png)

```blocks3
na zawsze
koniec
jeśli < > to
koniec
klawisz (v) wciśnięty?

zmień [uwaga v] o ()

ustaw [uwaga v] na []

po kliknięciu flagi
```

\--- /hint \--- \--- hint \---

This is what your code should look like:

![stage](images/stage.png)

```blocks3
kiedy flaga kliknęła
zawsze
ustaw [uwaga v] na [0]
jeśli wciśnięto klawisz <(vv)? > a następnie
zmiana [uwaga v] o (1)
koniec
jeśli naciśnięty został klawisz <(cv)? > a następnie
zmiana [uwaga v] o (2)
koniec
jeśli naciśnięto klawisz <(xv)? > a następnie
zmiana [uwaga v] o (4)
koniec
jeśli naciśnięto klawisz <(zv)? > a następnie
zmiana [uwaga v] o (8)
koniec
koniec
```

\--- /hint \--- \--- /hints \--- \--- /task \---