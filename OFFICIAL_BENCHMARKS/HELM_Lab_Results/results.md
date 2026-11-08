# HELM_Lab_Results — K_TACTICALMESH

**Run:** 2026-09-30T18:11:11.493145+00:00

```json
{
  "project": "K_TACTICALMESH",
  "seeds": [
    72583,
    3920,
    38119
  ],
  "seed_method": "sha256(name)[:8]+offsets[0,31337,65536]",
  "helm_standard": true,
  "run_ts": "2026-09-30T18:11:11.493145+00:00",
  "metrics": {
    "throughput_tokens_per_sec": {
      "seeds": [
        72583,
        3920,
        38119
      ],
      "values": [
        37.851,
        10.339,
        35.221
      ],
      "mean": 27.804,
      "std": 12.396,
      "ci_95_low": 3.508,
      "ci_95_high": 52.1
    },
    "latency_p50_ms": {
      "seeds": [
        72583,
        3920,
        38119
      ],
      "values": [
        83.973,
        30.286,
        46.917
      ],
      "mean": 53.725,
      "std": 22.44,
      "ci_95_low": 9.743,
      "ci_95_high": 97.707
    },
    "memory_mb": {
      "seeds": [
        72583,
        3920,
        38119
      ],
      "values": [
        32.651,
        77.491,
        56.697
      ],
      "mean": 55.613,
      "std": 18.322,
      "ci_95_low": 19.702,
      "ci_95_high": 91.524
    },
    "accuracy_score": {
      "seeds": [
        72583,
        3920,
        38119
      ],
      "values": [
        98.214,
        40.961,
        77.435
      ],
      "mean": 72.203,
      "std": 23.664,
      "ci_95_low": 25.822,
      "ci_95_high": 118.584
    },
    "f1_score": {
      "seeds": [
        72583,
        3920,
        38119
      ],
      "values": [
        53.633,
        72.309,
        16.578
      ],
      "mean": 47.507,
      "std": 23.161,
      "ci_95_low": 2.111,
      "ci_95_high": 92.903
    },
    "inference_tps": {
      "seeds": [
        72583,
        3920,
        38119
      ],
      "values": [
        41.893,
        86.392,
        58.676
      ],
      "mean": 62.32,
      "std": 18.348,
      "ci_95_low": 26.358,
      "ci_95_high": 98.282
    },
    "quality_score": {
      "seeds": [
        72583,
        3920,
        38119
      ],
      "values": [
        41.485,
        72.994,
        36.852
      ],
      "mean": 50.444,
      "std": 16.057,
      "ci_95_low": 18.972,
      "ci_95_high": 81.916
    }
  }
}
```
