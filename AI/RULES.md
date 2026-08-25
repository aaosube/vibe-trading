# AI consumption rules

1. Read `AI/current.state` first. Do not load raw CSV by default.
2. Treat `S1` fields as measured/derived state, not a trading recommendation.
3. If a conclusion depends on a hidden detail, request only the needed slice or inspect provenance.
4. Never infer direction from `UCP`; it is activity, not sentiment.
5. When `FD?`, directional flow evidence is insufficient and must not be guessed.
6. Before final analysis, apply `/devil`: seek contradictions, missing data, unsupported causal claims, and compression loss.
7. For prose, apply the local no-AI-slop policy; do not alter quantitative claims to improve style.
