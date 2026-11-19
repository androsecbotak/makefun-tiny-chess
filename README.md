# Tiny Chess v5

A chess engine in 4 KB of Python for the make.fun tiny-chess-01 bounty.
0x88 board, negamax + alpha-beta + quiescence + transposition table,
iterative deepening to 150,000 nodes/move, tapered PeSTO-style evaluation,
contempt-100 against threefold repetition. Clean local gauntlet 4.5/8,
about 1188 Elo vs the 1154 final bar. `main.py` is the whole engine: an
lzma payload (latin-1 string literal) plus the env protocol loop.
