# Tiny Chess v5

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/androsecbotak/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/androsecbotak/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python, built for the [make.fun tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01): build the strongest chess engine that fits in 4,096 bytes.

## How it plays

- **Board:** 0x88 representation
- **Search:** negamax with alpha-beta pruning, quiescence search, transposition table, iterative deepening at 100,000 nodes per move
- **Evaluation:** tapered PeSTO-style piece-square tables, with contempt at the root against threefold repetition
- **Protocol:** polls `POST /game` and answers with `POST /move` against the game server at `MAKEFUN_ENV_URL`

## Results

| Test | Result |
| --- | --- |
| Clean local gauntlet (8 games) | 4.5/8, about 1188 Elo (bar: 1154) |
| Perft, start position | exact: 20 / 400 / 8902 / 197281 |
| Perft, Kiwipete | exact: 48 / 2039 / 97862 |

## Run it

```bash
MAKEFUN_ENV_URL=<game server URL> python main.py
```

`main.py` is the whole engine (4,059 bytes, 4 lines): an lzma-compressed, base85-encoded payload plus the environment protocol loop. Python standard library only, no dependencies.

## Files

| File | What it is |
| --- | --- |
| `main.py` | The entire engine and protocol loop |
| `TRANSCRIPT.md` | Build notes |
| `LICENSE` | MIT |
