## Keeping score

To keep score, you’ll need somewhere to store the score, a way of adding to it, and a way of resetting it when the game is restarted.

+ First: storing it! Go to the **Data** blocks category and click **Make a Variable**.

![](images/catch5.png)

+ Enter `Score` as the name. 

![](images/catch6.png)

Check out your new variable and the blocks for it!

![The Score variable is displayed on the stage](images/scoreVariableStage.png)
![The blocks for the Score variable](images/scoreVariableBlocks.png)


--- collapse ---
---
title: What are variables?
---

When you want to store information in a program, you use something called a **variable**. Think of it like a box with a label on it: you can put something in it, check what’s in it, and change what’s in it. You’ll find variables under **Data**, but you need to create them first! 

--- /collapse ---


Now you need to update the variable whenever a fish is eaten, and to reset it when the game is restarted. Those are both pretty easy:

+ From the **Data** section, take the `set Score to 0`{:class="blockdata"} and `change Score by 1`{:class="blockdata"} blocks and put them into your program: 

### Code for the shark

```blocks
    when green flag clicked
    set [Score v] to [0]
    set rotation style [left-right v]
    go to x: (0) y: (0)
```

### Code for the fish

```blocks
    if <touching [Sprite1 v] ?> then
        change [Score v] by [1]
        hide
        wait (1) secs
        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
        show
    end
```

Cool! Now you’ve got a score and everything. 

--- challenge ---

## Challenge: winning the game

+ Pick a score at which the player wins, and make something cool happen. Maybe the shark congratulates them, or a "You win!" sprite appears, or music plays, or...you get the idea!

--- /challenge ---

