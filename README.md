# Maze Game Project

## Overview

This is a C++ console-based maze game where the player navigates a maze with obstacles and attempts to reach the goal while managing their lives and score. The game includes multiple levels with increasing complexity and features various actions such as movement, undo, and quitting.

### Game Features:
- **Maze Generation**: The maze is randomly populated with obstacles, and the player must navigate through it.
- **Movement Controls**: The player can move in four directions (up, down, left, right).
- **Undo Option**: The player can undo their last move.
- **Lives System**: The player starts with 3 lives. Each time they make an invalid move or retrace their steps, they lose a life.
- **Score System**: The player’s score is based on the number of steps taken to reach the goal. The fewer steps, the higher the score.
- **Level System**: There are multiple levels, and each level introduces a larger maze with more obstacles.
- **BFS Algorithm**: The shortest path to the goal is computed using a BFS (Breadth-First Search) algorithm for performance evaluation.

---

## Game Instructions

### Controls:
- **W**: Move up
- **A**: Move left
- **S**: Move down
- **D**: Move right
- **U**: Undo last move
- **Q**: Quit the game

### Objective:
- Navigate through the maze to reach the goal (denoted by `#`).
- Avoid obstacles (denoted by `X`).
- Each successful level completion increases the complexity of the maze.
- Manage lives and steps to maximize the score.

---

## Key Components

### 1. **Maze Generation**
The maze is represented as a 2D array of characters. Each cell can either be:
- Empty space (`' '`): The player can move here.
- Obstacle (`'X'`): The player cannot move here.
- Start point (`'@'`): The player's starting position.
- End point (`'#'`): The goal that the player needs to reach.

### 2. **Graph Representation**
A graph is used to model the maze and its connections. Each valid cell (not an obstacle) is treated as a node, and edges connect adjacent nodes if movement is allowed.

### 3. **Game Logic**
The game includes methods for:
- **Moving the player**: Checking if movement is possible and updating the player's position.
- **Undoing moves**: Retracing the player's previous steps.
- **Random obstructions**: Adding obstacles to the maze based on a specified percentage.
- **Scoring**: Calculating the player's score based on the number of steps taken and comparing it with the shortest path found.

### 4. **Levels**
Each level increases the size of the maze and the number of obstacles. The percentage of obstacles is also adjusted depending on the level.

---

## Class Breakdown

### 1. `Graph`
This class models the graph structure of the maze and includes methods for:
- Adding edges between nodes.
- Checking valid edges (i.e., non-obstructed paths).
- Using BFS to calculate the minimum steps from the start to the goal.

### 2. `mazegame`
This class contains the logic for the actual gameplay, including:
- Initializing the maze.
- Randomly placing obstacles.
- Drawing the maze on the console.
- Handling player movement and actions.
- Keeping track of the player's lives and score.

### 3. `Levels`
This class defines the difficulty levels by determining the percentage of obstacles in the maze for each level.

---

## How to Run the Game

1. **Compile the Code**:
   - Open your terminal or command prompt.
   - Navigate to the directory where the maze game file is located.
   - Run the following command to compile the code:
     ```
     g++ maze.cpp -o maze
     ```

2. **Run the Game**:
   - After compiling, run the game with:
     ```
     ./maze
     ```

3. **Follow the Instructions**:
   - Enter your name when prompted.
   - Choose your moves using the controls listed above.
   - Complete the maze and try to reach the highest score by minimizing the number of steps!

---

## Contributions

If you would like to contribute to this project, feel free to:
- Fork the repository.
- Submit pull requests with new features, improvements, or bug fixes.

---

## License

This project is open source and available under the MIT License. See the LICENSE file for more information.

---

## Acknowledgments

- The BFS algorithm was used to calculate the shortest path in the maze.
- The maze randomization and the game logic are built in C++ with a focus on simplicity and user interaction.
