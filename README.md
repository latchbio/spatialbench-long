# SpatialBench-Long

**Benchmarking long-horizon spatial biology**

This public subset contains four evals, their prompt/vocabulary files,
agent trajectory examples, and run results.

Paper: https://latch.bio/spatialbench-long

## Results

| Model | Harness | Runs | Passed | Pass Rate |
|---|---|---:|---:|---:|
| gemini-3.5-flash | pi | 72 | 8 | 11.11% |
| gpt-5.5 | openai-codex | 72 | 8 | 11.11% |
| gpt-5.5 | pi | 72 | 8 | 11.11% |
| claude-opus-4-6 | claude-code | 72 | 7 | 9.72% |
| claude-opus-4-7 | claude-code | 72 | 6 | 8.33% |
| grok-4.20-beta-0309-reasoning | pi | 72 | 5 | 6.94% |
| claude-opus-4-6 | pi | 72 | 4 | 5.56% |
| claude-opus-4-7 | pi | 72 | 4 | 5.56% |
| kimi-k2p6 | pi | 72 | 4 | 5.56% |
| gpt-5.4 | pi | 72 | 4 | 5.56% |
| claude-sonnet-4-6 | pi | 72 | 3 | 4.17% |
| gemini-3.1-pro-preview | pi | 72 | 3 | 4.17% |
| gpt-5.4 | openai-codex | 72 | 3 | 4.17% |
| grok-4.3 | pi | 72 | 3 | 4.17% |
| gemini-2.5-pro | pi | 72 | 1 | 1.39% |

## Citing

```bibtex
@misc{spatialbench-long-2026,
  title  = {SpatialBench-Long: Benchmarking Long-Horizon Spatial Biology},
  year   = {2026},
  url    = {https://github.com/latchbio/spatialbench-long}
}
```

## License

Apache 2.0 - see [LICENSE](LICENSE).
