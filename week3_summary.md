# Week 3 Summary: Data quality, labels, and leakage

## Cross-Book Summary

### 1. Systematic Data Cleaning (Neuer Ch 3)
- **The Cleaning Pipeline:** Handling NaNs, missing data (interpolation), and duplicates.
- **The "Fix at Source" Principle:** Digital cleaning is a last resort. Physical improvements to the measurement chain (sensors, environments) are preferred.
- **Normalization:** Essential for numerical stability in NNs, but must be done consistently between training and inference to avoid "scaling leakage."

### 2. The Annotation Problem (ML-PC Index, Field Experience)
- **Label Uncertainty:** In materials science, the "ground truth" is often subjective (e.g., manual grain boundary identification).
- **Inter-annotator Variance:** Different experts may segment the same micrograph differently. This variance sets an upper bound on meaningful model performance.

### 3. Data Leakage in Materials Science (ML-PC Index, Scientific Literature)
- **Spatial Leakage:** High correlation between different regions of the same physical sample. Randomly splitting pixels or patches into train/test results in over-optimistic performance. **Solution:** Split by sample or batch.
- **Temporal Leakage:** Using future process data to predict past outcomes in a time-series. **Solution:** Use "sliding window" or "walk-forward" validation.
- **Information Leakage:** Including features that are indirectly derived from the target variable.

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: The Quality Crisis (Slides 1-10)
- "Garbage In, Garbage Out": Case studies of ML failure due to bad data.
- The cost of data acquisition vs. the cost of bad labels.

### Part 2: Data Preprocessing & Cleaning (Slides 11-25)
- Systematic cleaning (Neuer Ch 3).
- Imputation strategies: Linear interpolation vs. Physics-based constraints.
- Normalization and Scaling: Min-Max, Z-score, and Robust scalers.

### Part 3: Labeling Microstructures & Signals (Slides 26-35)
- The human element: Manual annotation and its pitfalls.
- Quantification of label uncertainty.
- Crowdsourcing vs. Expert consensus in materials science.

### Part 4: Data Leakage: The Silent Killer (Slides 36-45)
- Definition: Information from the test set influencing the training.
- Spatial Correlation: The "Same Sample" trap.
- Feature Leakage: The importance of independent variables.
- How to detect leakage: The "Too good to be true" heuristic.

### Part 5: Robust Validation (Slides 46-50)
- Grouped K-Fold validation.
- Nested Cross-Validation.
- Summary: A checklist for a "Correct" materials ML pipeline.

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 3:**  
This unit focuses on the most critical and often overlooked part of the ML pipeline: data integrity. We discuss systematic data cleaning and normalization techniques while highlighting the unique challenges of labeling experimental materials data, such as inter-annotator variance. A major focus is on **Data Leakage**, specifically how spatial and physical correlations in materials samples can lead to deceptively high model performance. We introduce robust validation strategies to ensure models generalize to truly unseen data.
