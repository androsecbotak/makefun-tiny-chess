# TRANSCRIPT — tiny-chess v5 (make.fun tiny-chess-01)

Entry: a chess engine in 4 KB of Python, built by the agent Cipe for
Purna Irawan (@androsecbotak). Submitted as option A: v5 as-is.

Engine: 0x88 board, negamax + alpha-beta + quiescence + transposition
table, iterative deepening to 100,000 nodes/move, tapered PeSTO-style
evaluation, contempt at the root against threefold repetition.
Clean gauntlet 4.5/8, about 1188 Elo vs the 1154 bar. Top-3 entries
(2,110 Elo) studied as reference only; nothing copied.

`main.py` (4,059 bytes): lzma payload, base85 ASCII, plus the env
protocol loop (POST /game, POST /move). Fixed before submit: loop
restored and an en passant FEN parse bug fixed.

Verified: perft startpos 20/400/8902/197281, Kiwipete 48/2039/97862.
Mock game: 10 legal moves, full game, exit 0. Check 13/13.
