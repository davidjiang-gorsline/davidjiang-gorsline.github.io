---
layout: page
title: Research
---

I study contextualised forecasting: how to forecast trajectories when the most informative context arrives in unstructured text and the timing of impact is uncertain. The core challenge is to align events to downstream trajectories without leaking the future, while preserving robust evaluation under regime shifts. I aim to build methods and benchmarks that make forecasting systems auditable, reliable, and directly deployable.

## Timing-uncertain context

When context arrives in bursts (news, filings, reports), the impact can be delayed, smeared, or nonlinear. The modelling question is not just *what* changed, but *when* it should affect the forecast.

**Technical questions**
- How do we identify latent delays without overfitting to hindsight?
- What regularisers keep impact kernels interpretable and stable?
- How do we separate short-lived spikes from persistent regime shifts?
- What negative controls detect spurious alignment?

**Artifacts built**
- Alignment benchmarks, synthetic delay suites, and reference kernels for stress testing.

## Selective memory & retrieval

Context grows fast and relevance decays. Retrieval systems must decide *what to remember* and *when to abstain* as regimes drift.

**Technical questions**
- How should retrieval be calibrated to measurable retrieval error?
- How do gating/abstention policies trade off recall vs. noise?
- What regime prototypes are stable enough to anchor retrieval?
- Can we quantify retrieval drift over time?

**Artifacts built**
- Retrieval evaluation harnesses, regime-aware retrieval baselines, and controlled-memory ablations.

## Reliability & evaluation

Forecasting requires strict as-of timelines and temporal discipline. Evaluation must be leak-proof, revision-aware, and robust to data quality stress.

**Technical questions**
- How do we encode embargoes to prevent latent leakage?
- How should evaluation handle data revisions and late corrections?
- Which perturbations best proxy deployment failure modes?
- How do we calibrate reliability under multi-modal dropout?

**Artifacts built**
- Walk-forward evaluation harnesses, revision-aware replay tools, and perturbation suites.

## Current focus

- Joint modelling of delayed context impacts with retrieval calibration.
- Robust walk-forward benchmarks with stress-tested leakage controls.

## Open directions

- Identifiability guarantees for delay kernels with noisy context.
- Benchmarks for retrieval error under non-stationary regimes.
- Standardised negative controls for multimodal alignment.
