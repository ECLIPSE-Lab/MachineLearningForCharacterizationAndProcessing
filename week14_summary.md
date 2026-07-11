# Week 14 Summary: Course Recap — From Materials Data to Trustworthy Models

## Cross-Book Summary

### 1. The Course in One Map
- **One Arc:** raw materials data → representations → models → uncertainty and trust.
- **Units 1–3 (Data foundation):** small data, measurement chains, leakage-safe validation.
- **Units 4–5 (Representation):** stereology to learned embeddings; unsupervised clustering.
- **Units 6–9 (Learning under constraints):** transfer learning, time series, inverse problems, spectral signals.
- **Units 10–12 (Modern architectures & trust):** transformers, physics-informed constraints, uncertainty quantification.

### 2. The Four-Question Framework
Every unit is recapped through four checkpoints:
1. **What question** did it solve?
2. **What method & central equation** answers it?
3. **When do you reach for it** — and where does it break?
4. **What must you be able to do** in the exam?

### 3. The Decision Guide
- Twelve real lab scenarios mapped to method and unit, e.g.:
  - Small tabular data with error bars → Gaussian Process (U12).
  - Streaming sensor data, decisions on forecasts → probabilistic LSTM (U7).
  - Long-range image correlations, pretraining available → ViT (U10).
  - Known PDE, sparse sensors → PINN (U11).
  - No labels at all → clustering / autoencoders (U5).
- **Two precursor questions:** "Where did this data come from?" (U1–3) and "How wrong can I afford to be?" (U12).

## 90-Minute Lecture Strategy

### Part 1: The Map
- The 14-week / 12-unit arc as one data-to-trust pipeline.

### Part 2: Unit-by-Unit Recap
- Each unit's question, method, equation, and failure modes.

### Part 3: Synthesis
- The decision-guide table: task → tool → unit.
- Exam scope and mini-project rubric.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 14:**
- Recaps Units 1–12 with a four-question framework (question, method & equation, when to use, exam competence).
- Provides a decision guide mapping twelve lab scenarios to the right method and unit.
- Anchors deployment on two questions: data provenance and acceptable error budget.
- Closes with exam scope and the mini-project rubric: ML amplified the materials scientist, it did not replace them.
