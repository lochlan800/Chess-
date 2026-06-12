# Chess

A complete chess game in a single HTML file — no dependencies, no build step.
Open `index.html` in any browser and play against the computer.

## Features

- **5 difficulty levels**, from Beginner (shallow search with deliberate
  mistakes) to Master (deep minimax search with alpha-beta pruning and
  quiescence search)
- Full chess rules: castling, en passant, pawn promotion (with piece picker),
  check, checkmate, stalemate, 50-move rule, threefold repetition, and
  insufficient material draws
- Play as White or Black (board flips automatically)
- Legal move hints, last-move and check highlighting
- Move history, captured pieces, and material advantage display
- Undo button

## How it works

The engine uses a hand-written move generator (validated against standard
perft test positions) and a negamax search with alpha-beta pruning,
piece-square-table evaluation, MVV-LVA move ordering, and iterative deepening
with a per-level time budget. Lower levels search shallower and add random
noise to move scores so they play like a human beginner rather than a
crippled computer.
