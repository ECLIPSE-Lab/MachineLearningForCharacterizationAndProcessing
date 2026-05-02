# Week 8 Summary: Generalization, robustness, and process windows

## Cross-Book Summary

### 1. The Generalization Problem
- **Over/Underfitting:** Balancing high variance (noise fitting) vs. high bias (too simple).
- **Tradeoff:** Minimizing total error = Bias² + Variance + Noise.
- **Regularization:** L1 (Lasso) and L2 (Ridge) penalize complex models.

### 2. Robust Validation
- **Cross-Validation:** K-Fold provides stable performance estimates.
- **Leave-One-Out (LOO):** For extremely small datasets.
- **Stratification:** Maintains representative class/property distributions.

### 3. Process Robustness & Windows
- **Sensitivity Analysis:** Quantifying output change vs. input perturbation.
- **Process Windows:** Finding optimal, stable regions insensitive to industrial noise.
- **Robust Design:** Choosing stability over a sharp performance peak.

## 90-Minute Lecture Strategy

### Part 1: Reliability
- High accuracy is insufficient for deployment.
- Defining "Model Trust".

### Part 2: Bias/Variance
- U-shaped error curve.
- Visualizing overfitting.
- Double Descent.

### Part 3: Robust Validation Workflows
- K-Fold, Stratified, Grouped CV.
- Nested CV.
- Reliability metrics.

### Part 4: Regularization
- L2 (Ridge) and L1 (Lasso).
- Early Stopping.

### Part 5: Process Windows
- Mapping safe processing zones.
- Sensitivity analysis applications.
- Casting/3D Printing stability.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 8:**  
- Shifts focus from performance to Model Reliability.
- Explores Bias-Variance tradeoff and generalization.
- Details robust validation (K-Fold, Stratified CV).
- Uses sensitivity analysis to map stable Process Windows.