# Market State Compiler

Purpose: keep high-volume market data outside the LLM context. Compile vendor CSV exports into a small deterministic state plus full provenance.

## Run locally

```bash
python -m pip install -r market_state/requirements.txt
python market_state/compiler.py /path/to/csv-folder --output AI --symbol TSLA
python market_state/devil.py AI
```

The AI reads `AI/current.state`. It reads `AI/current.provenance.json` only when it needs an audit trail. It reads raw CSV only for a targeted forensic query, backtest, or explicit verification.

## Data policy

This repository is public. Do not commit licensed/vendor raw market-data exports here unless their terms explicitly permit redistribution. Keep real raw files local or in a private data store. Commit code, schema, tests, and compact derived state only.
