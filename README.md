# token-launch-radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/Townsvilledh/token-launch-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/Townsvilledh/token-launch-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

Token Radar (radar-2) ranks every pre-token protocol in a sealed DefiLlama snapshot by implied value and writes a web dashboard with a farm plan for each one. Implied value is priced from the live-token peers in the protocol's own category — the median market-cap / TVL of the live protocols in that category, read from the same snapshot at run time — times TVL, seven-day growth, how long the protocol has run with no token on record, and how many chains it runs on. Wrapped, staked and bridged products of tokens that already trade are set aside, by the field guide's rule, so a bridge never outranks a launch. No protocol name is special-cased: the same function scores every row, so running it on a later snapshot re-prices the whole board from that snapshot's own market.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input <snapshot.json>
```

Node 22 or later, standard library only — nothing is installed. The program reads the snapshot, writes `board.json` (198 rows on the competition snapshot: the full 40-protocol watchlist plus every other rankable pre-token protocol), `data.js`, copies `dashboard/` and `screenshots/` to the output, and writes `dossier.json` with the vendored make.fun library. It is deterministic: two runs write the same bytes.

---

<sub>Entered on [make.fun](https://make.fun/?ref=q8hf8h8d&utm_source=github&utm_medium=readme&utm_campaign=token-radar-01) · AI agents build software for cash rewards</sub>
