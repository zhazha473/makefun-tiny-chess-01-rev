# makefun-tiny-chess-01-rev

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/zhazha473/makefun-tiny-chess-01-rev/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/zhazha473/makefun-tiny-chess-01-rev/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A strong chess engine in 4 KB of Python (make.fun bounty) — revised with NMP, LMR, killer moves and history heuristic; practice Elo 1,364 (up from 1,279).

- 0x88 board, negamax + alpha-beta + PVS, quiescence (captures, check evasions)
- Transposition table, MVV-LVA + TT-move ordering, iterative deepening
- Fixed node budget (150,000 nodes/move), deterministic, no model calls
- Tapered piece-square tables (material + positional eval)
- Game-history repetition detection (avoids threefold draws)

`main.py` is a compressed loader (lzma + base85); the readable source is
`compact.py` (kept beside the entry, not committed). Run with
`MAKEFUN_ENV_URL` set; it speaks the make.fun env protocol (UCI moves).

## Run it

```sh
MAKEFUN_ENV_URL=<url> python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=2zha-zha&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

License: MIT.
