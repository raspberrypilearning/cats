## Cloning cats

We want to generate an infinite stream of cats that the player will guide along the path to the exit.

--- task ---
Click on the sprite called **Cat**, and add some code to make it invisible, and also to clone it every three seconds.

![Cat sprite](images/cat-sprite.png)

```blocks
when flag clicked
hide
forever
    create clone of [myself v]
    wait (3) secs
end
```

--- /task ---


If you run the program at the moment, nothing will happen. Let's make each cloned cat appear and fall out of the sky, so we can check that a new one is being created every three seconds.

--- task ---
Add some code to tell the sprite that when it starts as a clone, it should become visible and fall until it reaches the blue floor which is drawn on the stage.

![Cat sprite](images/cat-sprite.png)

--- hints ---
--- hint ---
`When the sprite starts as a clone`{:class="blockcontrol"}  `show`{:class="blocklooks"} the sprite. `Repeat`{:class="blockcontrol"} this until it `touches`{:class="blocksensing"} the blue stage. `Change`{:class="blockmotion"} the y coordinate of the sprite by `-2`.
--- /hint ---

--- hint ---
Here are the code blocks you'll need:

```blocks
repeat until <>
end

show

<touching color [#0000ff]?>

change y by (-2)

when I start as a clone
```
--- /hint ---

--- hint ---
This is what your code should look like:

```blocks
when I start as a clone
show
repeat until <touching color [#0000ff]?>
change y by (-2)
end
```

--- /hint ---
--- /hints ---

--- /task ---

When you press the green flag, you should see a new cat falling out of the sky every three seconds and landing in a big pile of overlapping cats on the blue floor at the bottom.

![Falling cats](images/falling-cats.png)
