---
layout: page
title: David Jiang-Gorsline
subtitle: Applied AI / Statistical ML for contextualised forecasting (text + time series), with leakage-aware evaluation.
---

**Now:** I lead applied ML in capital markets, building end-to-end forecasting systems that unify retrieval, evaluation, and deployment. My work focuses on disciplined experimentation, leakage-safe evaluation, and shipping systems that survive non-stationarity.

## Research pillars

- **Timing-uncertain context & event-to-trajectory alignment.** Model latent delays, impact kernels, and identifiability when text events influence trajectories with unknown lags.
- **Selective memory & retrieval under non-stationarity.** Build abstaining/gated retrieval, regime prototypes, and measurable retrieval error to keep context relevant as regimes shift.
- **Reliability & evaluation discipline.** Enforce as-of timelines, walk-forward splits with embargoes, revision-aware replay, and stress tests (timestamp jitter, modality dropout).

## Selected proof points

- Retrieval-bounded earnings-doc pipeline with **<1% hallucination** in evaluation-focused summarisation.
- Walk-forward evaluation harness with embargoes, leakage checks, and perturbation tests.
- Large-scale feature discovery over **~650k time-series features** on distributed compute.
- Deterministic finetuning / data distillation in prior research with **~80% compute reduction**.
