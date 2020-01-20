## लाइनों में रहें

आप देख सकते हैं कि, यदि आप दो प्लेटफार्मों के बीच एक नीचा पुल बनाते हैं, या ऊपर की ओर ढलान वाली एक रेखा खींचते हैं, तो बिल्लियाँ प्लेटफार्म के ऊपर चलने के बजाय उसमें से निकल कर जाती हैं!

![प्लेटफॉर्म से चलकर जाती हुई बिल्लियाँ](images/cat-walk-through-platform.png)

\--- task \---

In the code for the cat sprite, add another loop before the `next costume`{:class="block3looks"} block. This time, the loop should tell the cat to move upwards by `2` until it is not touching blue.

![Cat sprite](images/cat-sprite.png)

\--- hints \--- \--- hint \---

The cat should `move up 2`{:class="block3motion"} `repeatedly until`{:class="block3control"} it is `not`{:class="block3operators"} `touching blue`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Here are the code blocks you need:

```blocks3
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

\--- /hint \---

\--- hint \---

This is what your code should look like:

```blocks3
when I start as a clone
show
repeat until <touching (edge v)?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    repeat until <not <touching color [#0000ff]?>>
        change y by (2)
    end
    next costume
    wait (0.1) seconds
end
delete this clone
```

\--- /hint \---

\--- /hints \--- \--- /task \---

\--- task \---

Click the green flag and try drawing a line that slopes upwards. Check that your cat follows this line.

\--- /task \---