# SpatialBench-Long

**Benchmarking long-horizon spatial biology**

Scientists use spatial biology data in open-ended scientific contexts to
construct new knowledge about living systems.

SpatialBench-Long evaluates AI agents on their ability to arrive at conclusions
one might publish in a scientific journal, using the raw data and context a
scientist would have.

This public subset contains four evals, their prompt/vocabulary files,
agent trajectory examples, and run results.

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

## Included Evals

| Eval ID | Prompt/Vocabulary | Trajectory examples |
|---|---:|---:|
| `opticnerve_merfish_spatial_colocalization_enrichment` | yes | 4 |
| `visium_perineural_proximity` | yes | 4 |
| `lineage_metastasis_multilayer_niche_mapping` | yes | 4 |
| `xenium_organoid_spatial_niche_disruption` | yes | 4 |

The public trajectory examples contain 16 runs total. Each example includes
`trajectory.json`, `eval_answer.json`, and `result.json`. Intermediate generated
analysis files from agent workspaces are intentionally excluded.

## Introduction

Benchmarking long-horizon spatial biology presents new challenges:

- Spatial data is processed through multi-step analysis workflows, often
  integrated with other assay data.
- Information about the experimental design and prior literature might be used
  at each turn.
- Raw data rarely admits single scientific ground truths.
- Different conclusions can be drawn from the same dataset, often influenced by
  the original scientific goal of the study.
- Each conclusion can come from multiple valid and branching analysis paths.

## Benchmark Construction Methodology

- Randomized peer attempts
- Verifiable grading with controlled vocabularies
- Manual trajectory inspection as a first-class process

### Randomized Peer Attempts

Each eval was passed through randomized peer attempts without solutions. This
stress-tests design decisions in ground-truth values and task context. It also
calibrates agent performance against domain experts.

### Verifiable Grading With Controlled Vocabularies

Higher-level scientific claims move beyond numerical grading to written
conclusions about new biological facts. Grading relies on large controlled
vocabularies mixed with distractors of increasing specificity.

### Manual Trajectory Inspection

Future models may solve some evals using unanticipated analysis paths that break
current grading assumptions. Manual inspection of trajectories, aided by LLM
judges, is part of the benchmark workflow.

## Repository Contents

- `evals/` - public task prompts and vocabularies for the four included evals.
- `trajectories/` - trajectory JSON, final answers, and run results for
  selected eval/model/trial runs.

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
