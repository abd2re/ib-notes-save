---
tags: [EE] 
---
Created: 2022-12-12

Connect-4 comes in form of a game board, with 6 rows and 7 columns where different colored tokens are stacked. Two players play against each other with the objective to align 4 tokens of the same color, horizontally, vertically or diagonally like in Tic-Tac-Toe \cite{mf}. Each player successively slides his token so the game is a **zero-sum game** which is a term used in game-theory in which a person's gain is equivalent to another's loss. The Connect-4 grid can be represented as a matrix and the tokens can be represented with different values like 0 being an empty slot, 1 being the first player and 2 the second player (see Fig.1). This matrix representation of the Connect-4 board with a 2d array makes it easy for the computer to play moves, analyse the board and check for winning moves.

(FIG 1)

Approximately 4.5 trillions board configurations are possible for this game and are categorized as a moderate complexity game \cite{indians}. When will have to increase the grid size for the experiment, we will choose $n\times n+1$ dimensions with $n$ being an even number to have even numbers of rows and odd numbers of columns that relate back to the fundamentals of Connect 4 where there is a middle column.