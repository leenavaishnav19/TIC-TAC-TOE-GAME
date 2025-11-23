# TIC-TAC-TOE-GAME
# Tic-Tac-Toe 

A simple two-player Tic-Tac-Toe game implemented in Python for the command line. This project is designed as a beginner-friendly example of game logic, input validation, and basic data structures.

## Features

- 3x3 Tic-Tac-Toe board displayed with row and column indices.
- Two human players: 'X' and 'O', taking turns.
- Input validation for:
  - Correct format (row col)
  - Numeric values
  - Valid range (0–2)
  - Preventing moves on occupied cells
- Win detection for:
  - All rows
  - All columns
  - Both diagonals
- Draw detection when the board is full and no player has won.

## Requirements

- Python 3.x
- A terminal/console capable of reading standard input and printing text.

No third-party libraries are required.

## How to Run

1. Save the script as tic_tac_toe.py.
2. Open a terminal in the directory containing the file.
3. Run: tic_tac_toe.py

text

4. Follow the on-screen instructions:
- When prompted, enter your move as:

  
  row col
  

  Example:

  
  1 2
  

5. The game ends when:
- A player gets three of their marks in a row, column, or diagonal, or
- All cells are filled and the game is a draw.

## Internal Structure

- create_board(): Creates and returns a 3x3 list-of-lists board initialized with spaces.
- print_board(board): Prints the current state of the board with indices and separators.
- check_win(board, player): Checks whether the given player ('X' or 'O') has won by:
- Completing any row
- Completing any column
- Completing either main diagonal
- check_draw(board): Returns True if all cells are filled and no winner is found.
- get_player_input(player, board): Handles user input, validates it, and returns a valid (row, col) pair.
- play_game(): Main game loop that:
- Initializes the board
- Alternates between players
- Updates the board with each move
- Checks for win or draw and prints the final result

## Concepts Demonstrated

- Lists and nested lists to represent a grid-based board.
- Loops and conditionals for game flow and state checking.
- Functions for modular and readable code.
- Basic user input handling and validation.

## Possible Extensions

- Add a computer (AI) opponent using strategies or algorithms (e.g., minimax).
- Keep score across multiple rounds.
- Add an option to play again without restarting the script.
- Create a GUI version using libraries like Tkinter or Pygame.
