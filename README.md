# tiny-chess-01

A strong chess engine in 4 KB of Python (make.fun bounty).

- 0x88 board, negamax + alpha-beta + PVS, quiescence (captures, check evasions)
- Transposition table, MVV-LVA + TT-move ordering, iterative deepening
- Fixed node budget (150,000 nodes/move), deterministic, no model calls
- Tapered piece-square tables (material + positional eval)
- Game-history repetition detection (avoids threefold draws)

`main.py` is a compressed loader (lzma + base85); the readable source is in
`dev/compact.py` (see the builder's working directory). Run with
`MAKEFUN_ENV_URL` set; it speaks the make.fun env protocol (UCI moves).

License: MIT.
