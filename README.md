# JavaFX Pacman Game

A JavaFX implementation of the classic Pacman arcade game featuring intelligent ghost AI, multiple game modes, and authentic gameplay mechanics.

## Features

- **Classic Pacman Gameplay**: Navigate through a maze, collect dots and energizers while avoiding ghosts
- **Intelligent Ghost AI**: Four different colored ghosts with sophisticated pathfinding using Breadth-First Search (BFS) algorithm
- **Multiple Game Modes**:
  - **Chase Mode**: Ghosts actively pursue Pacman using different targeting strategies
  - **Scatter Mode**: Ghosts retreat to their respective corners
  - **Frightened Mode**: Ghosts move randomly and become vulnerable after Pacman eats an energizer
- **Dynamic Mode Switching**: Automatic transitions between game modes based on timers
- **Screen Wrapping**: Both Pacman and ghosts can wrap around the screen edges
- **Score System**: Points awarded for dots (10 pts), energizers (100 pts), and eating frightened ghosts (200 pts)
- **Lives System**: Start with 3 lives, lose one when caught by a ghost
- **Win/Lose Conditions**: Win by collecting all dots, lose when all lives are depleted

## Game Mechanics

### Ghost Behavior
Each ghost has unique targeting behavior in Chase mode:
- **Red Ghost**: Targets Pacman's exact position
- **Green Ghost**: Targets 3 squares behind and 1 square to the right of Pacman
- **Blue Ghost**: Targets 2 squares ahead of Pacman
- **Yellow Ghost**: Targets 4 squares to the left of Pacman

### Controls
- **Arrow Keys**: Move Pacman in the desired direction
- **Quit Button**: Exit the game

### Game Elements
- **Dots**: Small white circles worth 10 points each
- **Energizers**: Large white circles worth 100 points that make ghosts vulnerable
- **Walls**: Blue barriers that block movement
- **Ghost Pen**: Central area where ghosts respawn

## Technical Implementation

### Architecture
The game follows object-oriented design principles with clear separation of concerns:

- **App**: Main application entry point
- **PaneOrganizer**: Manages the overall UI layout
- **Game**: Core game logic and timeline management
- **Pacman**: Player character with movement and collision detection
- **Ghost**: AI-controlled enemies with pathfinding algorithms
- **MazeSquares**: Grid-based board representation
- **Collidable Interface**: Unified interface for interactive game objects (Dot, Energizer, Ghost)

### Key Algorithms
- **Breadth-First Search (BFS)**: Used for ghost pathfinding to find optimal routes to targets
- **Collision Detection**: Grid-based system for detecting interactions between game objects
- **Mode Management**: Timer-based system for switching between different ghost behaviors

### Data Structures
- **2D Array**: Represents the game board grid (23x23)
- **Queue**: Used in BFS algorithm for pathfinding
- **ArrayList**: Manages collidable objects in each grid square
- **Enum Classes**: Define game modes and movement directions

## Installation and Setup

### Prerequisites
- Java 8 or higher
- JavaFX runtime
- CS15 Support Library (included in package)

### Running the Game
1. Clone this repository
2. Ensure JavaFX is properly configured in your IDE
3. Run the `App.java` file
4. Use arrow keys to control Pacman and click "Quit" to exit

## Code Structure

```
pacman/
├── App.java                 # Main application class
├── PaneOrganizer.java       # UI layout manager
├── Game.java               # Core game logic and timeline
├── Pacman.java             # Player character implementation
├── Ghost.java              # AI ghost implementation with pathfinding
├── MazeSquares.java        # Grid square wrapper class
├── Collidable.java         # Interface for interactive objects
├── Dot.java                # Collectible dot implementation
├── Energizer.java          # Power pellet implementation
├── ScoreController.java    # Score and lives management
├── BoardCoordinate.java    # Immutable coordinate system
├── Direction.java          # Movement direction enum
├── Modes.java             # Game mode enum
└── Constants.java         # Game constants
```

## Demo

![Demo Video](assets/demo.gif)

## Credits

This implementation was created as a educational project for the introductory computer science class CSCI0150 at Brown University, inspired by the original Pacman arcade game developed by Namco.

## Note for recruiters

This project was developed in the context of a university class assignment. Due to academic integrity policies, the full source code cannot be made publicly available.

Recruiters and prospective employers may request private access or a demonstration of the code and results. Please reach out directly if you’d like to see more.

## Contact
Nina Py Brozovich
📧 nina_py_brozovich@brown.edu
