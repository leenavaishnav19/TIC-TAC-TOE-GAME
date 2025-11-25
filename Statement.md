# Tic-Tac-Toe Game - Project Statement

## Project Overview
**Application Name:** Tic-Tac-Toe (Noughts and Crosses)  
**Type:** Command-Line Game  
**Language:** Python 3  
**Mode:** Two-Player Local Multiplayer  
**Version:** 1.0  

## Purpose
This project implements the classic Tic-Tac-Toe game as a command-line application, providing an interactive gaming experience for two players. The application demonstrates fundamental programming concepts including game logic, input validation, win condition checking, and user interaction through a simple, intuitive text-based interface.

## Project Objectives

### Primary Goals
1. Create a fully functional two-player Tic-Tac-Toe game
2. Implement robust input validation and error handling
3. Provide clear visual feedback through board display
4. Detect all win conditions and draw scenarios
5. Deliver a smooth, user-friendly gaming experience

### Educational Goals
- Demonstrate modular function design
- Practice 2D list manipulation in Python
- Implement game state management
- Apply conditional logic and loop structures
- Handle user input validation comprehensively

## Technical Specifications

### Game Mechanics

**Board Structure:**
- 3x3 grid represented as a 2D list
- Each cell can contain: ' ' (empty), 'X', or 'O'
- Zero-indexed coordinate system (0-2 for both rows and columns)

**Player System:**
- Two players: 'X' and 'O'
- Player X always starts first
- Players alternate turns after each valid move

**Win Conditions:**
- **Horizontal Win**: Three identical marks in any row
- **Vertical Win**: Three identical marks in any column
- **Diagonal Win**: Three identical marks on either diagonal
  - Main diagonal: positions (0,0), (1,1), (2,2)
  - Anti-diagonal: positions (0,2), (1,1), (2,0)

**Draw Condition:**
- All 9 cells are filled with no winner present

### Core Functions

#### 1. `create_board()`
**Purpose:** Initialize a new game board  
**Returns:** 3x3 2D list filled with empty spaces  
**Usage:** Called once at the start of each game

#### 2. `print_board(board)`
**Purpose:** Display the current state of the board  
**Parameters:**
- `board`: Current game board (2D list)

**Output Format:**
```
   0   1   2
0  X | O |  
   ---|---|---
1    | X |  
   ---|---|---
2  O |   | X
```

**Features:**
- Column headers for easy reference
- Row numbers for coordinate identification
- Visual separators between cells
- Clean, readable layout

#### 3. `check_win(board, player)`
**Purpose:** Determine if specified player has won  
**Parameters:**
- `board`: Current game board
- `player`: Player to check ('X' or 'O')

**Algorithm:**
1. Check all three rows for horizontal wins
2. Check all three columns for vertical wins
3. Check main diagonal (top-left to bottom-right)
4. Check anti-diagonal (top-right to bottom-left)

**Returns:** Boolean (True if player has won)

#### 4. `check_draw(board)`
**Purpose:** Determine if the game is a draw  
**Parameters:**
- `board`: Current game board

**Logic:** Iterates through all cells; returns False if any empty cell found

**Returns:** Boolean (True if board is full)

#### 5. `get_player_input(player, board)`
**Purpose:** Get and validate player move  
**Parameters:**
- `player`: Current player ('X' or 'O')
- `board`: Current game board

**Validation Steps:**
1. Check input format (two space-separated values)
2. Verify both values are numeric
3. Confirm coordinates are within range (0-2)
4. Ensure selected cell is empty

**Error Messages:**
- Invalid format: "Invalid input. Please enter TWO numbers separated by a space."
- Non-numeric input: "Invalid input. Please enter NUMBERS for row and col."
- Out of range: "Coordinates out of range. Must be 0, 1, or 2."
- Cell occupied: "That cell is already taken! Try again
