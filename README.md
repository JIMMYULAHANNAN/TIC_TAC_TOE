Its a Game

This code is a simple implementation of the Tic Tac Toe game using Python. Below is a detailed explanation of the various components and the flow of the game:

### 1. **Displaying the Board**
   The function `display_board(board)` is used to print the current state of the Tic Tac Toe board. It takes the `board` list (representing the 3x3 grid) and formats it into a readable structure. Each element of the `board` represents a position on the grid, where `x` and `o` are the player's markers, and spaces are empty positions.

### 2. **Player Input**
   The function `player_input()` asks the first player to choose between 'x' or 'o' as their marker. Based on the first player's choice, the second player is automatically assigned the other marker. The function ensures that only valid inputs ('x' or 'o') are accepted.

### 3. **Placing the Marker**
   The `place_marker(board, marker, position)` function updates the board by placing the player's marker at the specified position. It replaces the empty space (' ') at the given index with the player's marker.

### 4. **Checking for a Win**
   The `win_check(board, mark)` function checks if the current player has won the game. It checks all possible win conditions in the Tic Tac Toe game (rows, columns, and diagonals). If any of the winning conditions are met (i.e., three markers of the same type in a row), it returns `True`.

### 5. **Randomly Choosing the First Player**
   The `choose_first()` function uses a random number generator to decide whether Player 1 or Player 2 will go first. It simulates a coin flip to choose between the two players.

### 6. **Checking for Empty Spaces**
   The `space_check(board, position)` function checks if a given position on the board is empty (i.e., contains a space ' '). This is used to ensure that players can only place markers on empty spots.

### 7. **Checking for a Full Board**
   The `full_board_check(board)` function checks whether the board is full, meaning there are no empty spaces left. If the board is full and no player has won, it results in a tie game.

### 8. **Player’s Turn**
   The `player_choice(board)` function prompts the current player to choose a position (from 1 to 9) on the board to place their marker. It ensures that the player selects a valid position and that the spot is not already occupied.

### 9. **Replay Option**
   The `replay()` function asks if the players want to play another game. If the answer is 'Yes', the game will restart; otherwise, the program ends.

### 10. **Game Loop**
   The main game loop starts with the message "Welcome to Tic Tac Toe". Players are asked to choose their markers and who will go first. After that, the game begins:

   - The game alternates turns between Player 1 and Player 2.
   - On each turn, the board is displayed, and the current player chooses a position to place their marker.
   - After each move, the game checks if the current player has won using `win_check()`. If a player wins, a message is displayed, and the game ends.
   - If the board is full but no player has won, it results in a tie, and the game ends.
   - After each round, the players are given the option to replay the game. If they choose to play again, the board is reset, and the process repeats.

### 11. **Break Condition**
   The `while` loop continues running the game until the `replay()` function returns `False`, indicating the players do not wish to play again. When that happens, the game ends.

### Summary of Gameplay:
- The game alternates between two players, where each player places either an 'X' or an 'O' marker on a 3x3 grid.
- The game checks after each move to see if there’s a winner or if the board is full (resulting in a tie).
- Players can choose to play multiple rounds without restarting the program.

code:
