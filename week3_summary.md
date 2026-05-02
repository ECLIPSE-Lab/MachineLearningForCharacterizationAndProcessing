# Week 3 Summary: Data quality, labels, and leakage

## Cross-Book Summary

### 1. Systematic Data Cleaning
- **Pipeline:** Handle NaNs, missing data, and duplicates.
- **Fix at Source:** Prefer physical improvements over digital cleaning.
- **Normalization:** Ensure consistent scaling between training and inference.

### 2. The Annotation Problem
- **Label Uncertainty:** Ground truth is often subjective.
- **Inter-annotator Variance:** Human disagreement sets an upper performance bound.

### 3. Data Leakage
- **Spatial Leakage:** Split by sample, not randomly, to avoid physical correlation.
- **Temporal Leakage:** Use sliding windows for time-series data.
- **Information Leakage:** Exclude features derived from targets.

## 90-Minute Lecture Strategy

### Part 1: Quality Crisis
- "Garbage In, Garbage Out".
- Cost of acquisition vs. bad labels.

### Part 2: Preprocessing & Cleaning
- Systematic cleaning.
- Imputation strategies.
- Scalers (Min-Max, Z-score).

### Part 3: Labeling
- Manual annotation pitfalls.
- Quantifying label uncertainty.
- Crowdsourcing vs. Experts.

### Part 4: Data Leakage
- Test data influencing training.
- Spatial and Feature leakage.
- "Too good to be true" heuristic.

### Part 5: Robust Validation
- Grouped K-Fold validation.
- Nested Cross-Validation.
- ML pipeline checklist.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 3:**  
- Emphasizes data integrity, cleaning, and normalization.
- Highlights materials annotation challenges like inter-annotator variance.
- Details Data Leakage risks from physical/spatial correlations.
- Introduces robust validation to ensure true generalization.