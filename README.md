# Tiny Chess v5

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/cariuang15/tiny-chess-04/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/cariuang15/tiny-chess-04/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty ($500 in USDC, 20 places paid). Pure standard library: 0x88 board, negamax + alpha-beta, quiescence search, iterative deepening on a fixed node budget (100,000 nodes/move, deterministic), transposition table with Zobrist hashing, MVV-LVA + killer ordering, material + piece-square eval with bishop-pair bonus, and game-history repetition handling. v5 builds on v4 (practice Elo 2,112, perfect 6/6): it adds the bishop pair (+30), Zobrist hashing, and a repetition fix — and drops the mate book, since the final uses fresh openings. `main.py` is 3,671 bytes (packed with the kit's `makefun compress`).

## Local results

- Fresh seed 3, 8 games vs the house gauntlet: **7.0/8, Elo 1,845** (v4: 6.0/8, Elo 1,669) — v5a beats nodes-2M, which v4 lost.
- Official practice trial-0: **6.0/6, Elo 2,112 (perfect)**, without the mate book.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=csc1bejp&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
