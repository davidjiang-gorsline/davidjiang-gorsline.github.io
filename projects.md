---
layout: page
title: Projects
---

## Retrieval-bounded LLM summarisation system ("QuickTake"-style)
**Problem:** Summaries that overfit or hallucinate when context is sparse.
**Approach:** Retrieval-bounded generation with strict evidence attribution and abstention.
**What shipped:** Earnings-doc summarisation pipeline with traceable evidence.
**Evaluation discipline:** Human-verified attribution, adversarial prompt probes, and doc-level recall checks.
**Metrics:**
- <1% hallucination rate in evaluation-focused audits.
- 95+% evidence coverage on targeted QA prompts.

## Leakage-safe walk-forward evaluation harness
**Problem:** Forecasting systems quietly leak future information in pipelines.
**Approach:** As-of timelines, embargoes, and revision-aware replay in a deterministic harness.
**What shipped:** A repeatable evaluation system for model/feature experiments.
**Evaluation discipline:** Embargo windows, perturbation tests, and automated leakage checks.
**Metrics:**
- 100% reproducible runs under versioned data snapshots.
- Leakage checks integrated into CI gates.

## Large-scale lag/lead feature discovery (~650k features)
**Problem:** Discovering predictive temporal structure at scale.
**Approach:** Distributed feature discovery with pruning, alignment checks, and stability filters.
**What shipped:** A scalable feature mining pipeline across multi-asset time series.
**Evaluation discipline:** Walk-forward stability tests and regime-specific validation.
**Metrics:**
- ~650k candidate features screened across assets.
- 10x reduction to stable, interpretable feature sets.

## Cross-asset recommendation / ranking engine
**Problem:** Prioritising cross-asset signals for portfolio decision support.
**Approach:** Learning-to-rank with latency-aware features and regime gating.
**What shipped:** A ranking engine feeding daily decision workflows.
**Evaluation discipline:** Out-of-sample rank correlation and as-of evaluation.
**Metrics:**
- Material uplift in top-k rank correlation vs. baseline heuristics.
- Latency budget enforced across feature set.

## Climate event platform (spatiotemporal ingestion + exposure mapping)
**Problem:** Connecting environmental events to asset exposure and risk.
**Approach:** Spatiotemporal ingestion, geocoding, and exposure mapping.
**What shipped:** Event ingestion and exposure dashboards with API access.
**Evaluation discipline:** Spatial accuracy audits and coverage completeness checks.
**Metrics:**
- Multi-source ingestion with validated geo-accuracy thresholds.
- Coverage improvements tracked across event types.

## Deterministic finetuning / data distillation (compute reduction)
**Problem:** High compute cost for finetuning experiments.
**Approach:** Deterministic finetuning and data distillation for efficient training.
**What shipped:** Reproducible finetuning pipeline with compute-aware configs.
**Evaluation discipline:** Controlled ablations and regression baselines.
**Metrics:**
- ~80% compute reduction versus baseline training.
- Stable performance under deterministic replay.
