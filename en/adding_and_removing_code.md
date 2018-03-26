## Adding code

Great! You’ve written your first Scratch program. Time to learn a little more about getting code in and out of Scratch! Scratch code is made up of **blocks** that you snap together to make programs.

These blocks come from the **Code Blocks Pallet** where they are broken up into different categories. By clicking on the category names, you can see the blocks in that category. Here, the **motion** category is selected.

![](/images/categories_and_code.png)

All of the blocks in the selected category are shown in a list. You can pick the one you want, click on it and hold down the mouse button, then just drag it onto the **current sprite panel** and let go.

Once the block is in the **current sprite pane** you can move it around and snap it to other blocks. If you want to see what a block does, you can double-click on it and it will run!

Normally, you want your blocks to run automatically, when something happens. This is why most of your programs will start with a block from the **events** category. Most often, it will be this one:

    ```blocks
    when green flag clicked
    ```
The code blocks connected to this block will run after the green flag is clicked

Code blocks run from top to bottom, so the order you snap your code together in matters.

In this example, the sprite will **say** “Hello!” before it will **play** the _meow_ sound.
    
    ```blocks
    when green flag clicked
    say [Hello!]
    play sound [meow]
    ```