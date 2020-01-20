## Podvoji mačke

Kar želiš, je neskočni tok mačk, ki jih mora igralec povesti vzdolž poti, do izhoda.

\--- task \---

Click on the sprite called 'Cat', and add some code to `hide`{:class="block3looks"} the sprite, and also to `clone`{:class="block3control"} it every three seconds.

![Cat sprite](images/cat-sprite.png)

```blocks3
when flag clicked
hide
forever
    create clone of (myself v)
    wait (3) seconds
end
```

\--- /task \---

If you run the program now, nothing happens on the Stage. To check that a new Cat sprite clone is created every three seconds, make each clone appear and fall out of the sky.

\--- task \---

Add code to tell the sprite that `when it starts as a clone`{:class="block3control"}, it should `show`{:class="block3looks"} itself and fall until it `touches`{:class="block3sensing"} the blue floor that is drawn on the Stage.

![Cat sprite](images/cat-sprite.png)

\--- hints \--- \--- hint \---

`When the sprite starts as a clone`{:class="block3control"}, `show`{:class="block3looks"} the sprite. `Repeatedly`{:class="block3control"} `Change`{:class="block3motion"} the sprite's `y` coordinate by `-2`, until the sprite `touches`{:class="block3sensing"} the blue Stage.

\--- /hint \---

\--- hint \---

Here are the code blocks you need:

```blocks3
ponavljaj do <>
konec

pokaži

<se dotika barve [#0000ff]?>

spremeni y za (-2)

ko začnem kot dvojnik
```

\--- /hint \---

\--- hint \---

This is what your code should look like:

```blocks3
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

When you click the green flag, you should see a new cat fall from the top of the Stage every three seconds. Every cat should land in a big pile of overlapping cats on the blue floor at the bottom.

![Falling cats](images/falling-cats.png)