## Cloning cats

We want to generate an infinite stream of cats that the player will guide along the path to the exit.

+ Click on the sprite called **Cat**, and add some code to make it invisible, and also to clone it every three seconds.

![Clone a cat](images/clone-a-cat.png)

If you run the program at the moment, nothing will happen. Let's make each cloned cat appear and fall out of the sky, so we can check that a new one is being created every three seconds.

+ Add some code to tell the sprite that when it starts as a clone, it should become visible and fall until it reaches the blue floor which is drawn on the stage

--- hints ---
--- hint ---
`When the sprite starts as a clone`  `show` the sprite. `Repeat` this until it `touches` the blue stage. `Change` the y coordinate of the sprite by `-2`.
--- /hint ---

--- hint ---
Here are the code blocks you'll need:

![Drawing with the pen hint](images/falling-cat-hint.png)
--- /hint ---

--- hint ---
This is what your code should look like:
![Drawing with the pen solution](images/falling-cat-solution.png)
--- /hint ---

--- /hints ---

When you press the green flag, you should see a new cat falling out of the sky every three seconds and landing in a big pile of overlapping cats on the blue floor at the bottom.

![Falling cats](images/falling-cats.png)
