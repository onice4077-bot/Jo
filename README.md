# Solitaire Solver

An intelligent automated program for playing and solving Klondike Solitaire games through computer vision and artificial intelligence.

## Overview

This project combines computer vision, OCR, and heuristic algorithms to automatically detect, analyze, and solve Klondike Solitaire games. The solver can process images of Solitaire games, recognize cards, and execute optimal moves to reach a solution.


## Key Features

### 🎮 Game Solving Engine
- Advanced heuristic-based solver for determining optimal moves
- Priority-based decision making that considers:
  - Maximizing empty tableau spaces
  - Uncovering face-down cards
  - Building foundation sequences

### 🔍 Computer Vision System
- **Robust Card Detection**
  - Advanced contour detection for identifying card boundaries
  - Precise location and orientation recognition
  - Support for overlapping and partially visible cards
  
- **Accurate Card Recognition**
  - Suit classification using ORB (Oriented FAST and Rotated BRIEF) feature matching
  - Value recognition through Tesseract OCR integration
  - Support for all standard playing cards (A, 2-10, J, Q, K)

### 🤖 Automation
- Seamless game interaction through PyAutoGUI
- Automated mouse movement and clicking for card manipulation
- Real-time move execution based on solver decisions


**Limitations:** The heuristic-based solver works well for most Solitaire setups but does not guarantee the optimal solution or solve every game, particularly in more complex configurations. The card recognition accuracy depends on the quality of the input image and the clarity of the cards.

## Gameplay Examples


https://github.com/user-attachments/assets/2d7def7b-a6d9-4990-adb8-68377b515390


The video demonstrates the Solitaire Solver automatically detecting cards and making optimal moves to solve a Klondike Solitaire game, showcasing real-time game interaction and move execution.

## Installation

To use the Solitaire Solver, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/supat-roong/solitaire_solver.git
   
  got clone  https://github.com/onice4077-bot/Jo.git
   
   ```
2. Navigate to the project directory:
   ```bash
   cd solitaire_solver
   
   
   
   cd Jo
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Install Tesseract OCR (if not already installed):
   - **Linux**: 
     ```bash
     sudo apt-get install tesseract-ocr
     ```
   - **Windows**: Download the installer from [here](https://github.com/tesseract-ocr/tesseract) and follow the installation instructions.
   - **macOS**: 
     ```bash
     brew install tesseract
     ```

## Usage

1. Open your favorite Solitaire game.
2. Run the solver:

```bash
python main.py
```

3. Use the selection tool to select the game board region.
4. The program will automatically solve the game!

## Debug Visualization
This project also includes a built-in debugger for each computer vision step, allowing you to visualize card detection and recognition in real-time.



https://github.com/user-attachments/assets/d495185b-d6e5-4b60-9123-358017f5449b


## Project Structure
The project is organized as follows:

```
solitaire_solver/
├── src/                          # Source code directory
│   ├── config.py                 # Configuration file for solver parameters and settings
│   ├── custom_dataclass.py       # Defines custom data structures used throughout the project
│   ├── debugger.py               # Provides debugging tools
│   ├── image_processor.py        # Handles image preprocessing and card detection
│   ├── player.py                 # Automates gameplay (mouse control and decision execution)
│   ├── screenshot.py             # Captures the screen region containing the Solitaire game
│   ├── solver.py                 # Implements the heuristic-based Solitaire solving algorithm
├── media/                        # Stores media files used in the project
│   └── card_suits/               # Contains template images for card suits classification
└── main.py                       # Main entry point for running the solver

```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
