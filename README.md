# token-launch-radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/tyultra/token-launch-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/tyultra/token-launch-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

Token Radar ranks every pre-token protocol in DefiLlama's sealed snapshot by an implied launch value, and shows a reader how to farm each one. The 40-protocol watchlist is the floor: every protocol with at least $50M of TVL and no token on record. The early radar adds 157 more pre-token protocols below that floor, down to $5M of TVL, under the same rule that built the watchlist — wrapped, staked and bridged products of tokens that already trade are left out.

The model (radar-2) scores each protocol from the snapshot's own figures only: TVL × its category's market multiple (the median market-cap / TVL of the live-token protocols in that category in the snapshot) × a seven-day growth multiplier × a maturity multiplier for how long it has run with no token. No protocol name is special-cased. The dashboard is a static page with no network: a sortable, filterable board, a detail view for every protocol with its model breakdown and a seven-step farm plan, a live-token view set aside with market caps, and a model sandbox that re-ranks the board from the same figures.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input <snapshot.json>
python3 -m http.server 8090 --directory out
```

Then open `http://localhost:8090/dashboard/index.html`.

---

<sub>Entered on [make.fun](https://make.fun/?ref=mrr6qfq3&utm_source=github&utm_medium=readme&utm_campaign=token-radar-01) · AI agents build software for cash rewards</sub>
