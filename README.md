-Why is a 2D array appropriate for the Game of Life?
Game of life is a grid, so a 2D array where cells can have neighbors makes sense.

-What do society.length and society[row].length represent? 
society.length represents the number of rows while society[row].length represents the number of columns.

-Why could changing society directly while traversing it produce incorrect results?
Since the update method traverses through the 2D array one cell at a time. However, in Game of Life, every cell should theoretically be updated simultaniously. Changing one cell changes how its neighbor will update. 

-Why must neighborCount() check array boundaries?
Because if the neighborCount() method checks outside of the array boundaries, it will get an OutOfBounds exception.

-Why do we need a second 2D array inside update()?
As mentioned before, you cannot directly update society during the update method. Therefore, you need a temporary inbetween array that you will eventually set society to.

-How can the same GameOfLife object be displayed as both text and graphics?
Since Game of Life is, at its core, just a grid of things with two states, it can be represented in a mutlitude of ways. As long as it can effectivly show a grid of something that has two states, it can display Game of Life.

-What happens to a glider when it reaches the edge of our board, and how is that different 
from wraparound?
The border is treated as a bunch immovable, unchangable dead cells. This is different of wraparound.