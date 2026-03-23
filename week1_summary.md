# Week 1 Summary: What makes materials data special?

## Cross-Book Summary

### 1. The Concept of Data-Based Modeling (Neuer, Sandfeld, McClarren)
- **Data-based vs. First-Principle Models:** In engineering, we traditionally rely on first-principle models (bottom-up, derived from axioms like Newton's laws). Machine Learning introduces data-based modeling (top-down), where the model is extracted from observed process data.
- **Traceability (White, Grey, Black Boxes):** First-principle models are "White-Box" (fully explainable). ML models are often labeled "Black-Box," though techniques for "Grey-Box" (hybrid) and explainability are emerging to build scientific trust.
- **Overfitting:** A historical perspective (Sandfeld) shows that even Aristotle's 56-sphere model of the heavens was a form of overfitting—being too complex for the task at hand.

### 2. Foundations of Data (Neuer, Bishop)
- **Data Types:** Nominal (names/categories), Ordinal (ordered), Cardinal (numeric), and Binary.
- **Scales:** Nominal, Ordinal, Interval (e.g., Celsius), and Ratio (e.g., Kelvin with absolute zero). Understanding the scale is critical for correct normalization and interpretation.
- **Units and Uncertainty:** Experimental data is meaningless without units and an estimation of measurement uncertainty.

### 3. Materials Science Specifics (ML-PC index, Sandfeld)
- **The PSPP Paradigm:** Processing–Structure–Property–Performance forms a dependency graph. Materials data is inherently multi-scale and multi-modal (images, spectra, logs).
- **Experimental Noise:** Unlike "clean" toy datasets, materials data contains physical noise, sampling artifacts (aliasing), and biases from instrument resolution.
- **Data Scarcity:** Obtaining high-quality materials data is slow and expensive, making standard "big data" approaches often inapplicable.

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: Introduction & Philosophy (Slides 1-10)
- Course goals and the AI 4 Materials program.
- The "Hype Cycle" vs. Reality in scientific AI.
- Why now? The convergence of high-throughput experiments, simulation, and ML.

### Part 2: Models in Engineering (Slides 11-20)
- Defining a "Model": Prediction vs. Explanation.
- First-Principles (physics-based) vs. Data-Driven approaches.
- The Black-Box stigma and the move toward White-Box ML.

### Part 3: What Makes Materials Data Special? (Slides 21-35)
- The PSPP Chain as a data graph.
- Types of data: Micrographs (pixels), EBSD (orientations), EDS (spectra), Process logs (time-series).
- The "Small Data" problem in Materials Science.
- Physical Priors: How physics limits the possible data space.

### Part 4: Data Foundations & Quality (Slides 36-45)
- Categorizing data: Nominal, Ordinal, Cardinal.
- The critical role of Metadata and Units.
- Measurement uncertainty and its propagation into ML models.

### Part 5: The CRISP-DM Workflow for Labs (Slides 46-50)
- Adapting the industrial standard to the materials lab.
- From "Scientific Understanding" to "Deployment" in production.
- Correlation != Causality (The Ice Cream and Crime rate example).

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 1:**  
This unit introduces the transition from classical physics-based modeling to data-driven discovery in materials science. We explore the unique challenges of experimental materials data, including its multi-modal nature, high acquisition cost, and the fundamental Processing-Structure-Property-Performance (PSPP) relationships. Key concepts include data scales, measurement uncertainty, and the CRISP-DM process adapted for scientific workflows.
