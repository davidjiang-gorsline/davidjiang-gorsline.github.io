---
layout: post
title: "As-of evaluation, embargoes, and revision-aware replay"
tags: [forecasting, evaluation, leakage]
---

Evaluating forecasting systems is hard because data arrives in waves and gets revised. An as-of evaluation harness encodes the data that was actually observable, while embargoes prevent implicit leakage from post-event artifacts. This note sketches the minimal components that make the evaluation trustworthy.

**Claims / takeaways**
- As-of timelines must be encoded for every modality and every feature.
- Embargoes should be explicit, not implicit in training splits.
- Revision-aware replay catches subtle backfills that inflate metrics.
- Leakage checks are most effective when automated and repeated per run.

## How to test it

- Compare metrics using live-as-of snapshots vs. backfilled datasets.
- Add controlled embargo windows (e.g., 1-5 days) and measure robustness.
- Introduce synthetic revisions and verify performance stability.
