# Minesweeper 💣

A classic, text-based version of the Minesweeper game implemented in Python.

## Project Overview

* The game is played on a customizable `n x n` grid with a specified number of hidden mines.
* The objective is to reveal all the cells that do not contain a mine.
* If you select a cell with a mine, you lose! If you reveal all safe cells, you win.


## Game Flow

The game follows a loop structure that continues until the game is either won or lost. In each iteration of the loop, the following steps occur:

1. Display the current state of the Minesweeper grid.

2. Accept input from the player, allowing them to select a cell or flag a cell as a mine.

3. Handle player input and update the grid accordingly.

4. Check if the game is over (either won or lost).

5. If the game is over, display the appropriate message and end the game.

### Screenshots

Starting Grid: <br>
<img width="618" height="542" alt="image" src="https://github.com/user-attachments/assets/f0339e93-794a-4b7a-a26c-9328b3d6c6e2" /> <br>

Error: <br>
<img width="775" height="110" alt="image" src="https://github.com/user-attachments/assets/b6b1884d-5fef-47be-846a-3cdfbf51773d" />

Flagging a mine: <br>
<img width="553" height="630" alt="image" src="https://github.com/user-attachments/assets/96468630-cf70-4523-af39-25366f15cfd8" />

Win end screen: <br>
<img width="544" height="669" alt="image" src="https://github.com/user-attachments/assets/b3f5a371-59d0-41b1-ad04-3bcf4383a27e" />

Loss end screen: <br>
<img width="546" height="671" alt="image" src="https://github.com/user-attachments/assets/95a7ba53-4666-4006-a3bc-0cbaf65a1715" />



## Features

* **Classic Gameplay**: Uncover cells and avoid the hidden mines.
* **Customizable Difficulty**: Easily change the grid size (`n`) and number of mines (`mines_no`) in the script.
* **Flagging System**: Mark cells you suspect contain mines with an 'F'.
* **Automatic Area Clearing**: Selecting a cell with zero neighboring mines will automatically clear all adjacent empty cells.
* **Win/Loss Detection**: The game automatically detects when you've won or lost.


## Code Overview

The game is built with several key functions:

* `print_mines_layout()`: Renders and displays the current state of the game board in the terminal.

* `set_mines()`: Randomly places the specified number of mines on the grid at the start of the game.

* `set_values()`: Calculates the numbers for the non-mine cells based on how many mines are adjacent to them.

* `neighbours(r, col)`: A recursive function that reveals all adjacent cells when a cell with a value of '0' is selected.

* `check_over()`: Checks if the win condition (all non-mine cells revealed) has been met.

* `show_mines()`: Reveals the locations of all mines when the game is over (either by winning or losing).
