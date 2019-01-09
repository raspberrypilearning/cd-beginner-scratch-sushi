## Keeping score

To keep score of how many fish the player catches, you’ll need somewhere to store the score, a way of adding to it, and a way of resetting it when the game is restarted.

+ First: storing the score! Go to the **Variables** blocks category and click on **Make a Variable**.

![](images/catch5.png)

+ Enter `score` as the name. 

![](images/catch6.png)

Check out your new variable!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)

--- collapse ---
---
title: What are variables?
---

When you want to store information in a program, you use something called a **variable**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. You’ll find variables in the **Variables** section, but you need to create them first for them to show up there! 

--- /collapse ---

Now you need to update the variable whenever the shark eats a fish, and to reset it when the game is restarted. Doing both is pretty easy:

+ From the **Variables** section, take the `set [my variable v] to [0]`{:class="block3variables"} and `change [my variable v] by [1]`{:class="block3variables"} blocks. Click on the little arrows in the blocks, choose `score` from the list, and then put the blocks into your program: 

### Code for the shark

![blocks_1546569190_9005241](images/blocks_1546569190_9005241.png)

### Code for the fish

![blocks_1546569191_975879](images/blocks_1546569191_975879.png)

Cool! Now you’ve got a score and everything. 

--- challenge ---

## Challenge: winning the game

+ Pick a score at which the player wins, and make something cool happen. Maybe the shark congratulates them, or a "You win!" sprite appears, or music plays, or...you get the idea!

--- /challenge ---

