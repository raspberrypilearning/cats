## Drawing lines

--- task ---
Open the 'CATS!' Scratch starter project.

**Online:** open the starter project at [jumpto.cc/cats-go](http://jumpto.cc/cats-go){:target="_blank"}. If you have a Scratch account, you can click on **Remix** in the top right-hand corner to save a copy of the project.

**Offline:** open the [starter project](resources/cats-resources.sb2) in the offline editor. If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---
Click on the sprite called 'Pen', and add code to set the pen colour to the same blue as the obstacles on the Stage.

![Pen sprite](images/pen-sprite.png)

```blocks
when flag clicked
set pen color to [#0000ff]
clear
set pen size to (5)
```

To select a colour, click on the colour square in the `set pen color`{:class="blockpen"} block to make your mouse cursor turn into a pipette, and then click on the correct colour on the Stage.

--- /task ---

--- task ---
Add some more code to make the sprite follow the mouse pointer. Test your program to check that the code works.

![Pen sprite](images/pen-sprite.png)

```blocks
forever
go to [mouse pointer v]
end
```

[[[generic-scratch-saving]]]

--- /task ---

--- task ---
Add some code to tell the sprite to draw a line on the Stage if the mouse button is pressed down.

![Pen sprite](images/pen-sprite.png)

--- hints ---
--- hint ---
`If`{:class="blockcontrol"} the `mouse is down`{:class="blocksensing"}, put the `pen down`{:class="blockpen"}, and `else`{:class="blockcontrol"}, lift the `pen up`{:class="blockpen"}.
--- /hint ---

--- hint ---
Here are the code blocks you need:

```blocks
<mouse down?>

pen down

pen up

if <> then
else
end
```
--- /hint ---

--- hint ---
This is what your code should look like:

```blocks
when flag clicked
set pen color to [#0000ff]
clear
set pen size to (5)
forever
go to [mouse pointer v]
if <mouse down?> then
pen down
else
pen up
end
```
--- /hint ---

--- /hints ---
--- /task ---

--- task ---
Test your code. You should be able to click and drag with the mouse to draw a blue line on the Stage.

![Draw a line](images/draw-a-line.png)

--- /task ---

You probably see that a blue dot always appears in the top right-hand corner of the Stage (it's circled in the image above). This is because, when you click the green flag to start the game, you press the mouse down, and so the pen immediately starts drawing.

--- task ---
To stop this from happening, add a `pen up`{:class="blockpen"} block at the start of the script, and a `wait one second`{:class="blockcontrol"} block above the `forever`{:class="blockcontrol"} block.

![Pen sprite](images/pen-sprite.png)

```blocks
when flag clicked
+ pen up
set pen color to [#0000ff]
clear
set pen size to (5)
+ wait (1) secs
```
--- /task ---
