## Moving cats

When a cat has appeared and fallen until it reaches the floor, we want it to step slowly to the right.

--- task ---
Add some code to the `when I start as a clone`{:class="blockcontrol"} section to make the cat sprite `move ten steps`{:class="blockmotion"}, and switch between the two costumes every 0.1 seconds to make it look like the cat is walking.

![Cat sprite](images/cat-sprite.png)

--- hints ---
--- hint ---
The cat sprite should `move 10 steps`{:class="blockmotion"}, and `switch costume`{:class="blocklooks"} every `0.1 seconds`{:class="blockcontrol"}. This code (as well as the code to make the cat fall) should repeat `forever`{:class="blockcontrol"}.
--- /hint ---

--- hint ---
Here are the code blocks you'll need:

```blocks
move (10) steps

wait (0.1) secs

next costume

forever
end
```
--- /hint ---

--- hint ---
This is what your code should look like:

```blocks
when I start as a clone
show
forever
    move (10) steps
    repeat until <touching colour [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) secs
end
```

--- /hint ---

--- /hints ---
--- /task ---

--- task ---
Press the green flag and check that the cats now move along the blue platform at the bottom.
--- /task ---

You will notice that, if you draw a bridge across the gap so that the cats can get all the way to the right edge of the screen, they end up getting stuck walking into the wall.

![Flailing cats at the edge](images/flailing-at-edge.png)

--- task ---
Remove the forever loop you added, and instead add a different loop to make the cats only walk until they reach an edge. When a cat reaches the edge of the screen, it should disappear.

```blocks
when I start as a clone
show
+ repeat until <touching [edge v]?>
    move (10) steps
    repeat until <touching colour [#0000ff]?>
        change y by (-2)
    end
    next costume
    wait (0.1) secs
end
+ delete this clone
```

--- /task ---

--- task ---
Press the green flag and check that the cats disappear when they reach the edge of the screen.

You might notice that the cats don't disappear properly if they fall into the hole, they just get stuck at the bottom. This is because the sprite is getting stuck trying to fall!
--- /task ---

This is the code which tells the cat to keep falling until it touches blue. However, in the hole the cat will never reach blue, so it is stuck forever.

```blocks
repeat until <touching colour [#0000ff]?>
end
```

--- task ---
Add more blocks to this loop to tell it to repeat until it is touching blue `or`{:class="blockoperators"} `touching the edge`{:class="blocksensing"}. This way, the sprite will stop trying to fall if it reaches the edge of the screen.

```blocks
repeat until <<touching colour [#0000ff]?> or <touching [edge v]?>>
end
```

--- /task ---
