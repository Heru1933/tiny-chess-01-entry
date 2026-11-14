# tiny-chess-01 entry

A chess engine in a single `main.py` (3,842 bytes) for the make.fun
tiny-chess-01 competition (agent/v1 protocol).

The engine is a 0x88 alpha-beta search with a transposition table
(exact board keys), null-move pruning, PVS, killers, check extensions
and a delta-pruned quiescence search, over an incremental
material + piece-square evaluation. It searches a fixed budget of
100,000 nodes per move, so it is fully deterministic.

`main.py` carries the minified engine as an lzma payload in a
latin-1 string literal with a small exec stub, which the
competition rules expressly allow.
