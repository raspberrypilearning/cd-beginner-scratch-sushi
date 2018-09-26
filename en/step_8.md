## Fishing!

The shark moves, the fish swims, but they don’t interact: if the fish swims right into the shark's mouth, nothing happens. Time to change that!

First, you need to know if the fish is touching the shark. For this, you'll need a **Control** block and a **Sensing** block. 

+ Add the `if...then`{:class="blockcontrol"} **Control** block inside the `forever`{:class="blockcontrol"} loop of the fish sprite, below the `if on edge bounce`{:class="blockmotion"} block.

+ Drag the `touching...`{:class="blocksensing"} block into the space at the top of the `if...then`{:class="blockcontrol"} block, and click the little triangle to select the shark sprite's name. If you haven’t changed it, it'll be 'Sprite1'.

```blocks
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
    end
```

--- collapse ---
---
title: How does it work?
---

The `if...then`{:class="blockcontrol"} **Control** block needs to be given a `True/False` value. 

**Sensing** blocks collect information, like where the sprite is, what it’s touching, etc. You're using this block:

```blocks
    <touching [Sprite1 v] ?>
```

From this block's pointy ends, you can tell it’s going to give you the `True/False` value that the `if...then`{:class="blockcontrol"} block needs.

--- /collapse ---

Of course, you’ve just added an `if...then`{:class="blockcontrol"} block without adding anything for the 'then' part. So at the moment your script is checking whether the fish sprite is touching the shark sprite, but it's not making anything happen in response.

You can make the fish disappear, as if the shark ate it, by using the `hide`{:class="blocklooks"} block.

+ Find the `hide`{:class="blocklooks"} block in the **Looks** list, and put it inside the `if...then`{:class="blockcontrol"} block, like so: 

```blocks
    if <touching [Sprite1 v] ?> then
        hide
    end
```

Now once the shark catches the fish, the fish disappears for good. That’s not great.

+ Put the `show`{:class="blocklooks"} block from **Looks** in at the very start of the fish code, so you can reset the game. 

```blocks
    when green flag clicked
    show
    set rotation style [left-right v]
    forever
```

That's already better, but you don’t want the player to have to restart the game every time they catch a single fish! 

+ Update the code inside your `if...then`{:class="blockcontrol"} block to look like this:

```blocks
    if on edge, bounce
    if <touching [Sprite1 v] ?> then
        hide
        wait (1) secs
        go to x: (pick random (-240) to (240)) y: (pick random (-180) to (180))
        show
    end
```

--- collapse ---
---
title: How does this work?
---

You are being clever here: when the fish is hidden, it waits, moves, and then shows up again. 

It looks like lots of fish keep appearing, but it’s that one sprite moving around! 

--- /collapse ---

That’s a game! But there’s no way to keep score yet, or to win. You can fix that too — on the next card!
