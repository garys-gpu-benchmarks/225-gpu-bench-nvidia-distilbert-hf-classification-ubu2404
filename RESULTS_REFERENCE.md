# Results: 225 DistilBERT NLP Training Baseline

**Main goal:** Measure DistilBERT classification training throughput  
**Tools:** Run gpu-bench-distilbert-sst2-train.py via collect_distilbert_train.py

Reference results from the validation run on the system shown in each section (recorded 2026-11-22). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 80GB HBM3 (81559 MiB) · Intel(R) Xeon(R) Platinum 8470 · Ubuntu 24.04.5 LTS · kernel 6.8.0-149-generic · driver 595.112.07
- **Run:** 2026-11-22T11:19:13Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 01:33 · benchmark 00:01 · whole run 01:41
- **Source:** run 225_20261122_111913
- **Command:** `bash run_benchmark.sh --smoke --model-name distilbert-base-uncased --sequence-len 32 --batch-size 2 --learning-rate 5.0000000000000002E-5 --weight-decay 0.01 --num-iterations 2 --gradient-accumulation 1 --warmup-iters 1`

| # | Metric | Result |
|---|---|---|
| 1 | Training throughput (samples_per_sec) | 47.269274 |
| 2 | Training step time, ms (step_time_ms) | 42.310783 |
| 3 | Token throughput (tokens_per_sec) | 1512.616758 |
| 4 | Peak GPU memory (peak_gpu_memory_gb) | 1.411881 |
<!-- /profile:smoke -->
