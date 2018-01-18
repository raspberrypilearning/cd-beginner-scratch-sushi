## Moving things around

Now your scratch cat moves, but wouldn’t it be more fun to control it with the arrow keys? On this card, you’re going learn how to do that!

+ As you’ve probably guessed, you’re going to need **event** and **motion** blocks again! This time, you’re looking for this block: 

```blocks
    when [space v] key pressed
```

+ If you click the little arrow (▼) beside `space` you’ll get a list of all the keys on your keyboard to pick from. You’re going to need four of these blocks and you can connect them to **motion** blocks like this: 

```blocks
    when [left arrow v] key pressed
    move (-10) steps
```

```blocks
    when [right arrow v] key pressed
    move (10) steps
```

```blocks
    when [up arrow v] key pressed
```

```blocks
    when [down arrow v] key pressed
```

Note: -10 means: **go back 10 steps**


Your cat moves back and forwards now, which is pretty cool, but it doesn’t move up or down. Also, if you look through the **motion** blocks, you’ll see there are no blocks for “up” or “down”. There are a whole bunch of them related to **x** and **y** though...

When programmers need to talk about the positions of objects, like sprites, we often use **x** and **y** coordinates to describe them. The **x-axis** runs from left to right, while the **y-axis** runs from bottom to top. 

![](images/moving3.png)

A sprite can be located by the coordinates of its centre, written something like (15, -27) where 15 is the **x** position and -27 is the **y** position.

+ To get a feel for how this actually works, take the `go to`{:class="blockmotion"} block from motion and drop it onto your **sprite panel**. You don’t need to connect it to anything. 

```blocks
    go to x: (15) y: (-27)
```

+ Next, pick some values for **x** and **y**, fill them in, and **double click on the block**. Try different sets of values to see where the cat goes! In Scratch **x** goes from -240 to 240 and **y** goes from -180 to 180.

+ Now you know about **x** and **y** coordinates, you can make the cat move up and down! You just need to change its **y** value. You can update your code like this: 


```blocks
    when [left arrow v] key pressed
    move (-10) steps
```

```blocks
    when [right arrow v] key pressed
    move (10) steps
```

```blocks
    when [up arrow v] key pressed
    change y by (10)
```

```blocks
    when [down arrow v] key pressed
    change y by (-10)
```

Now when the arrows are pressed, the cat can move all over the stage!

The cat moves all over the screen, but imagine this is a game: How do you restart it? You need to get the cat back to its original location when the player starts the game. In Scratch, they start the game by clicking on the green flag, so you need to change the cat’s **x** and **y** coordinates when that happens.

That’s actually pretty easy! The centre of the stage is (0,0) in **x** and **y** coordinates. 

+ So all you need is an **event** block for that green flag and the **go to** block you’re already using. Set the `go to`{:class="blockmotion"} to `(0,0)` and then snap it to the flag event block. 

```blocks
    when green flag clicked
    go to x: (0) y: (0)
```