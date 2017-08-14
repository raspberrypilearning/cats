## Moving cats

- cats move, switch costume, and fall

When a cat has appeared and fallen until it reaches the floor, we want it to step slowly to the right.

+ Add some code to the **When I start as a clone** section to make the cat sprite move 10 steps and switch between the two costumes every 0.1 seconds to make it look like the cat is walking

![Two costumes](images/two-costumes.png)

--- hints ---
--- hint ---
The cat sprite should **move 10 steps**, then **switch costume** every **0.1 seconds**. This code (as well as the code to make the cat fall) should repeat **forever**.
--- /hint ---

--- hint ---
Here are the code blocks you'll need
![Moving cat hint](images/moving-cat-hints.png)
--- /hint ---

--- hint ---
This is what your code should look like:
![Moving cat hint](images/moving-cat-solution.png)
--- /hint ---

--- /hints ---

+ Run your code and check that the cats now move along the blue platform at the bottom.

You will notice that if you draw a bridge across the gap so that the cats can get all the way to the right edge of the screen, they end up getting stuck walking into the wall.

![Flailing cats at the edge](images/flailing-at-edge.png)

+ Remove the **forever** loop you added, and instead add a loop to make the cats walk and fall **until they are touching the edge**. Once they reach an edge, add a block to **delete the clone** which will make the cat disappear. 
