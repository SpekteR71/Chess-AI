# Chess-AI
A chess AI developed from scratch 

The UI, engine and the AI was created from scratch. I have uploaded three files viz. chessMain, chessEngine, chessAI. To play with the AI, run the chessMain.py file. Use 
'z' to undo a move and 'r' to reset the board.

ChessMain:
  This is driver code for the program. it contains the gamestate and code for event handling i.e. actions to be taken upon user input.

ChessEngine:
  The core of the program.
  Contains numerous functions to generate moves for each piece, validate the moves and return only legal moves.
  Functions to check for captures, pins, checks, checkmate, stalemate in adddition to various helper functions.
  Class containing move information. 
  
ChessAI:
  This file contains the code for getting the best move from AI in addition to getting a random move from the set of valid moves. The random move function was implemented
  to make the AI more beginner friendly. A simple minimax algorithm with alpha beta pruning was used to get the best move from the AI.
  
Observations:
  The AI played quite fast at a depth of 3 but lost 5/5 games against me (rated 1500). At a depth of 6, the AI took a considerably longer time to decide the best move 
  despite the use of alpha beta pruning but also performed considerably better drawing 3/3 games. It is nowhere near the level of an IM or even a CM but further work can
  be done to improve the AI's speed and accuracy.
  
Future Work:
  1. Implementing transposition tables to make the AI faster.
  2. Hsving separate evaluation functions for opening, middlegame, endgame.
  3. Could explore using reinforcement learning to update piece value and position evaluation.
  
  
  Edit: The AI's performance is rather impressive at depth 4, with the AI recognising threats pretty well. The true effect of alpha beta pruning can be seen in the             middlegame. The AI also makes book moves upto move 4 somtimes upto move 6 without having any explicit code recognising book moves. The AI performs rather   
        poorly in the endgame even with an equal position as it does not see enough moves ahead.
        
  Edit 2: Upon playing a few games at depth 5, I discovered a minor bug. Assume piece 1 blocks check and opponent gives another check in the next move with piece 1  
          still under pin, piece 1 is abe to move and block the second check. Other cases of pins seem to work fine.
          
