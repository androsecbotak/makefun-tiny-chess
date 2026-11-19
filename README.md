# Tiny Chess v5

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/androsecbotak/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/androsecbotak/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python for the [make.fun tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01).
0x88 board, negamax + alpha-beta + quiescence + transposition table,
iterative deepening to 100,000 nodes/move, tapered PeSTO-style evaluation.
Clean local gauntlet 4.5/8, about 1188 Elo vs the 1154 final bar.
`main.py` is the whole engine: an lzma payload (base85 ASCII) plus the
env protocol loop (polls /game, posts /move). Run it with
`MAKEFUN_ENV_URL` set to the game server URL.
