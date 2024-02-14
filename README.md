
# Maze Generator and Solver

This project is a C++ application that generates and solves a maze. You can either watch the program solve the maze automatically or navigate through it yourself using keyboard inputs. The maze generation is achieved through a randomized depth-first search algorithm, and the solution can be visualized step by step.

## Project Features

### Maze Generation

The maze is created using a randomized depth-first search (DFS) algorithm. This involves:

- **Initialization**: The maze is initially filled with walls (`#`).
- **Carving**: Starting from a specified point, the algorithm carves out passages by visiting neighboring cells in a random order. It uses a stack-based approach to backtrack when it hits a dead end.
- **Random Carving**: Additional random paths are created to increase complexity and provide multiple solutions.

### Maze Solving

Two options are available for solving the maze:

1. **Automatic Solving**: The program uses a recursive depth-first search to find a path from the start to the end of the maze. The path is marked with `*` and visualized on the console.
2. **Manual Navigation**: You can navigate through the maze using the keyboard controls (`W`, `A`, `S`, `D`).

### Console Display

- **Colored Output**: The solved path is highlighted in red.
- **Real-time Updates**: The maze is displayed in real-time as it is being solved or navigated.

### Interactive Options

Upon starting the program, you are prompted to:

1. **Input Dimensions**: Enter the number of rows and columns for the maze (with odd dimensions for better structure).
2. **Choose Mode**: Decide between automatic solving (Simulation) or manual play.

## Algorithms and Techniques

### Depth-First Search (DFS)

- **Maze Generation**: DFS is used to create a maze by recursively visiting and carving out cells.
- **Shuffling Directions**: The order of cell exploration is randomized using the `std::shuffle` function from the C++ Standard Library to ensure varied maze patterns.

### Recursive Backtracking

- **Maze Solving**: The solver uses recursive backtracking to explore all possible paths from the start to the end until it finds a solution or concludes that no solution exists.

### Randomized Carving

- **Enhancing Complexity**: After the primary maze is generated, additional random passages are carved to increase the complexity and provide a more challenging experience.

## Code Walkthrough

### Key Functions

- **`shuffleDirections`**: Randomizes the order of directions to explore during maze generation.
- **`isValid`**: Checks if a cell is within maze boundaries and is a wall that can be carved.
- **`printMaze`**: Outputs the current state of the maze to the console with optional coloring for the solution path.
- **`carveMaze`**: Recursively carves out the maze from a given starting point using DFS.
- **`randomCarve`**: Adds random paths to the maze to create multiple potential routes.
- **`solveMaze`**: Recursively finds a path through the maze using DFS, marking the path with `*`.
- **`playMaze`**: Allows the user to control the `*` character to navigate through the maze manually.

### Terminal Enhancements

- **`HIDE_CURSOR` and `SHOW_CURSOR`**: Control the visibility of the cursor during maze display to improve visual clarity.
- **`CLEAR_SCREEN`**: Clears the console before displaying the maze to ensure a clean output.
- **`RED` and `NORMAL`**: Define color codes for highlighting the solution path.

## Example Output

Here is a snapshot of the maze during the solving process:

```bash
#################
****************#
###############*#
#***************#
#* ##############
#*********      #
#########*####  #
#*********      #
#*#### ##########
#************   #
############*## #
#************   #
#*###############
#********       #
########*###### #
#       *********
#################
```

You can capture this output by running the program in a terminal and following the prompts to see the maze being solved or play through it manually.

## Conclusion

This project demonstrates the use of recursive algorithms and randomization techniques in generating and solving mazes. It provides both an automated solution and an interactive mode for users to experience the maze-solving process firsthand.

Enjoy exploring the mazes and happy solving!

---

Feel free to contribute to this project or suggest improvements. For more details, visit the project's [repository](https://github.com/Nishant-8009/maze.git).
