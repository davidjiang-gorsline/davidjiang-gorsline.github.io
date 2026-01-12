---
layout: post
title: "Temporal leakage in multimodal forecasting: a practical taxonomy"
tags: [forecasting, evaluation, multimodal, retrieval, leakage]
---

When text, events, and time series share a timeline, leakage is rarely a single bug. It is usually a layered failure across ingestion, labeling, alignment, and evaluation. This note outlines a compact taxonomy to help diagnose where leakage is most likely hiding.

**Claims / takeaways**
- Leakage often appears as *temporal slippage* rather than obvious feature lookahead.
- Multimodal pipelines leak through document availability, revision times, and delayed event coding.
- Alignment heuristics (nearest-neighbor, window joins) can silently encode future context.
- Evaluation harnesses must encode "as-of" boundaries for every modality.

## How to test it

- Run a timestamp jitter stress test (shift document timestamps forward/backward and track metric sensitivity).
- Compare model performance under strict embargo windows vs. permissive windows.
- Replay with revision-aware snapshots to ensure only information available at time *t* is used.
