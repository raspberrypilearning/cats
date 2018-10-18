## Getting to safety

The object of the game is to guide the cats to safety by creating a safe path for them to reach the door. Let's make a score variable to keep track of how many cats have successfully reached the door.

--- task ---
Create a variable called `score`{:class="blockdata"}.

![Cat sprite](images/cat-sprite.png)

[[[generic-scratch-add-variable]]]

--- /task ---

--- task ---
Add some code to your cat sprite to add one to the score each time a cat reaches the door. Don't forget to also set the score to zero at the start of the game.

![Cat sprite](images/cat-sprite.png)

--- hints ---
--- hint ---
`If`{:class="blockcontrol"} the cat is `touching the door sprite`{:class="blocksensing"}, then `add 1 to the score`{:class="blockdata"}.
--- /hint ---

--- hint ---
Here are the new code blocks you'll need to add:
```blocks
change [score v] by (1)

if <> then
end

set [score v] to (0)

<touching [Door v]?>
```
--- /hint ---

--- hint ---
This is what your code should look like:

```blocks
when I start as a clone
show
repeat until <touching [edge v]?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
    repeat until <not <touching color [#0000ff]?>>
        change y by (2)
    end
    next costume
    wait (0.1) secs
    + if <touching [Door v]?> then
        + change [score v] by (1)
    + end
end
delete this clone
```
--- /hint ---

--- /hints ---

--- /task ---

--- task ---
Add some more code so that a cat sprite that reaches the door makes a 'meow' sound and then disappears.

![Cat sprite](images/cat-sprite.png)

```blocks
play sound [meow v]
delete this clone
```
--- /task ---
