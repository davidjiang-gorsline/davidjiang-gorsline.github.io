---
layout: post
title: "Event-to-trajectory alignment with negative controls"
tags: [forecasting, evaluation, retrieval, multimodal]
---

Aligning events to downstream trajectories is not a simple join. Impact can be delayed, nonlinear, or transient, and naive alignment produces spurious correlations. Negative controls help validate whether the alignment pipeline is actually causal or just opportunistic.

**Claims / takeaways**
- Negative controls should include permuted event times and randomized entity mappings.
- Alignment should be evaluated under delay distributions, not fixed offsets.
- Identifiability improves with constrained impact kernels and regularisation.
- Retrieval relevance should be reported alongside forecast accuracy.

## How to test it

- Run alignment against permuted timestamps to measure spurious lift.
- Fit delay distributions and measure sensitivity to kernel regularisation.
- Introduce modality dropout to test reliance on single-event sources.
