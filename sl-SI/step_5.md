## Drži se črt

Morda opaziš, da kadar narišeš nizek most med ploščadima ali črto, ki gre navzgor, mačke hodijo skozi ploščad in ne po njej!

![Mačke gredo skozi ploščad](images/cat-walk-through-platform.png)

\--- task \---

In the code for the cat sprite, add another loop before the `next costume`{:class="block3looks"} block. This time, the loop should tell the cat to move upwards by `2` until it is not touching blue.

![Cat sprite](images/cat-sprite.png)

\--- hints \--- \--- hint \---

The cat should `move up 2`{:class="block3motion"} `repeatedly until`{:class="block3control"} it is `not`{:class="block3operators"} `touching blue`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Here are the code blocks you need:

```blocks3
<se dotika barve[#0000ff]?>

spremeni y za (2)

ponavljaj do <>
konec

ne <>
```

\--- /hint \---

\--- hint \---

This is what your code should look like:

```blocks3
ko začnem kot dvojnik
pokaži
ponavljaj do <se dotika (roba v) ?>
  pojdi (10) korakov
  ponavljaj do <se dotika barve [#0000ff] ?>
    spremeni y za (-2)
  end
  ponavljaj do <ne <se dotika barve [#0000ff] ?>>
    spremeni y za (2)
  end
  naslednji videz
  počakaj (0.1) sekund
end
zbriši tega dvojnika
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Click the green flag and try drawing a line that slopes upwards. Check that your cat follows this line.

\--- /task \---