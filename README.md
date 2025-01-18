# CodeAlpha-sudoko-Solver**
**Name** = Hasnain Mustafa **Company** = CodeAlpha 𝗦𝘁𝘂𝗱𝗲𝗻𝘁 𝗜𝗗: CA/JA1/9530 𝗗𝗼𝗺𝗮𝗶𝗻: C++ Programming 𝗗𝘂𝗿𝗮𝘁𝗶𝗼𝗻: 15th January 2025 to 15th February 2025
The program solves a partially filled Sudoku grid by recursively filling in the missing values while adhering to the game's constraints.

**Key Components**
1. **Grid Representation**
The Sudoku grid is represented as a 2D vector of integers, sudokuTable.
-1 indicates an empty cell.
Pre-filled numbers represent fixed values.
2. **Validation Function**
isValid(int row, int col, int value) checks whether placing a specific value in a given cell is valid:
Ensures the value does not already exist in the same row or column.
Checks the value's validity within the corresponding 3x3 subgrid.
3. **Backtracking Solver**
findSol(int row, int col, int& solCount) recursively tries to fill the grid:
Iterates through all potential values for empty cells.
If valid, places the value and moves to the next cell.
If the solution fails at any point, backtracks by resetting the current cell and trying the next value.
Stops when all cells are filled, increments the solution count, and prints the solution.
4. **Fixed Values Handling**
A set of fixedPairs stores the positions of pre-filled cells.
Ensures these values are not modified during the solving process.
5. **Solution Display**
printSol(int solCount) formats and prints each solution:
Includes dividing lines for the 3x3 subgrids to make the grid visually clear.
Execution Flow
Input Initialization:

A pre-defined Sudoku grid with some cells filled is loaded into sudokuTable.
Fixed Values Identification:

Positions of pre-filled cells are stored in fixedPairs.
Recursive Solving:

The findSol function begins at the top-left cell and attempts to solve the puzzle using backtracking.
Output Results:

Displays all valid solutions or a message indicating no solution exists.
Outputs the total number of solutions found.
Features
Handles Multiple Solutions:

The program doesn't stop at the first solution but continues to find and display all possible solutions.
Dynamic Validation:

Ensures that each number placed maintains the integrity of the Sudoku rules.
Formatted Output:

Solutions are printed in a user-friendly, grid-like format.
Potential Enhancements
User Input:

Allow the user to input custom Sudoku puzzles.
Difficulty Analysis:

Determine the difficulty of the Sudoku based on the number and position of fixed values.
Optimized Backtracking:

Implement heuristic techniques like Most Constrained Variable (MCV) to improve efficiency.
Puzzle Validation:

Add a function to validate the initial input grid (e.g., ensuring no rule violations exist before solving).
Educational Value
This project demonstrates:

Backtracking Algorithm: A systematic way to explore all possible solutions.
Constraint Satisfaction: Handling constraints dynamically during problem-solving.
2D Data Structures: Working with multi-dimensional vectors effectively.
Efficient Design: Using sets for constant-time lookups of fixed positions.
This is a great project for learning about algorithms, recursion, and problem-solving in C++.
