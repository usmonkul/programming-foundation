**Game On!  Building Your Own Games in Scratch**

Get ready to level up your Scratch skills, game developers! Today, we're diving into the exciting world of game creation. We'll learn how to use sensors, create interactive challenges, keep score, and even program a sprite that follows your mouse!

**Quick Review and Warm-up**

Before we start building games, let's quickly review some key concepts from our last session.

* **Costumes:** How do we change a sprite's appearance? (Answer: Using the `next costume` block)
* **Sound Effects:**  How do we add sound to our projects? (Answer: Using the `play sound` block)
* **Interactive Dialogue:** How do we make our sprites talk? (Answer: Using the `say` block)

**Warm-up Challenge:** Can you make a sprite change color when you click on it? (Hint: Use the `when this sprite clicked` block and a `change color effect` block)

**Building a Simple Game: Dodge the Obstacle!**

Let's create a game where a player controls a sprite to dodge a moving obstacle.

1. **Choose Your Sprites:** Select a sprite for your player (maybe a spaceship or a running character) and another sprite for the obstacle (like a falling rock or a moving enemy).
2. **Make the Obstacle Move:** Use a `forever` loop and `move` blocks to make the obstacle move across the Stage. You can even make it bounce off the edges using `if on edge, bounce` block.
3. **Player Control:** Use the `when key pressed` blocks to allow the player to move their sprite up and down or left and right.
4. **Sensing Blocks:** Now for the exciting part! We'll use **sensing blocks** to detect when the player touches the obstacle.
    * **`touching` block:** Drag a `touching` block from the "Sensing" category into your script.  Select the obstacle sprite from the dropdown menu.
    * **Game Over:**  Use an `if then` block to check if the player is touching the obstacle. If they are, you can make the player say "Game Over!" or switch to a "game over" costume.

5. **Keeping Score:**
    * **Create a Variable:** Go to the "Data" category and click "Make a Variable." Name your variable "Score."
    * **Increase the Score:**  Use the `change score by 1` block to increase the score every second or every time the player successfully avoids the obstacle.
    * **Display the Score:** Check the box next to "Score" in the "Data" category to display the score on the Stage.

**Loops and Repetition: Taking Control**

We already know about the `forever` loop. Now let's explore some more advanced loop options!

* **`repeat until` block:** This block repeats a section of code until a specific condition is met. For example, you could make a sprite repeat a movement until it touches a certain point on the Stage.
* **`forever` and `if then`:** Combining a `forever` loop with an `if then` block allows you to create more complex behaviors. For example:

   ```scratch
   forever
       if touching edge then
           turn 180 degrees
       end
       move 10 steps
   end
   ```

   This code makes the sprite move continuously and turn around whenever it touches the edge of the Stage.

**Challenge: Mouse Follower**

Can you create a sprite that follows your mouse pointer around the Stage? (Hint: Use the `forever` loop, the `go to` block, and the `mouse x` and `mouse y` blocks from the "Sensing" category.)

**Creative Game Design: Unleash Your Imagination!**

Now it's time to put your game design skills to the test! You can:

* **Modify the Dodge Game:** Add more obstacles, different levels, power-ups, or even a timer.
* **Create Your Own Game:** Design a completely new game! Think about the kind of game you want to make (a maze game, a catching game, a puzzle game) and use the blocks you've learned to bring your ideas to life.

**Teacher Support and Exploration**

Remember, I'm here to help you with any questions you have and to guide you as you explore new blocks and concepts. Don't be afraid to experiment and try new things! The most important thing is to have fun and unleash your creativity!
