# S1 compact market-state schema

Default LLM input is `AI/current.state`. Raw CSV is evidence storage, not prompt context.

- `PX` spot/last price
- `D` daily percent change
- `H`,`L` daily high/low
- `AH` last extended-hours minute price
- `VW` regular-session minute VWAP
- `GF` gamma-profile zero crossing nearest spot
- `CW` max call-gamma-exposure strike within ±15% of spot
- `PW` most-negative put-gamma-exposure strike within ±15% of spot
- `GR` gamma-profile sign at spot
- `IV`,`IR`,`IP` implied volatility, IV rank, IV percentile
- `PCV`,`PCO` put/call volume and OI ratios
- `FD` signed options-flow premium in millions; `?` when side coverage is insufficient
- `FC` fraction of total premium with bid/ask directional classification
- `UCP` unusual-options call/put volume ratio; activity only, not sentiment
- `Q` fraction of expected input roles discovered

Exact tokenization depends on the model. The compiler uses a conservative character-based estimate and `/devil` rejects states above the configured budget.
