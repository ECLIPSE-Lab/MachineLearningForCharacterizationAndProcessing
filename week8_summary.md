# Week 8 Summary: Generalization, robustness, and process windows

## Cross-Book Summary

### 1. The Generalization Problem (Neuer Ch 4, McClarren Ch 3)
- **Overfitting vs. Underfitting:** A model with too much flexibility (high variance) captures the noise in the training data, while a model that is too simple (high bias) fails to capture the underlying trend.
- **Bias-Variance Tradeoff:** The fundamental struggle in ML is finding the balance where the total error (Bias² + Variance + Noise) is minimized.
- **Regularization:** Techniques like L1 (Lasso) and L2 (Ridge) penalize overly complex models by adding a term to the loss function that discourages large weights (Bishop Ch 3).

### 2. Robust Validation (Sandfeld Ch 13, Neuer Ch 4)
- **Cross-Validation (CV):** Moving beyond the static train/test split. K-Fold CV provides a more stable estimate of model performance by rotating the validation set.
- **Leave-One-Out (LOO):** A specialized form of CV for extremely small materials datasets where every data point counts.
- **Stratification:** Ensuring that each fold is a representative "mirror" of the overall population in terms of class balance or property distribution.

### 3. Process Robustness & Windows (McClarren Ch 2, ML-PC Index)
- **Sensitivity Analysis:** Using the model's derivatives to quantify how much an output changes for a small perturbation in input ($\partial y / \partial x$).
- **Process Windows:** Identifying the region in parameter space where the material property is not only optimal but also **insensitive** to typical industrial noise (e.g., small fluctuations in temperature or pressure).
- **Robustness as a Design Criterion:** Choosing a process point that is slightly less "perfect" but much more "stable" compared to a peak that drops off sharply.

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: Reliability in Materials ML (Slides 1-10)
- Why "High Accuracy" is not enough for industrial deployment.
- The concept of "Model Trust": When does the user stop believing the prediction?

### Part 2: Bias, Variance, and Complexity (Slides 11-20)
- The U-shaped total error curve.
- Visualizing overfitting: Polynomial regression examples (McClarren Ch 2).
- The "Double Descent" phenomenon (briefly).

### Part 3: Robust Validation Workflows (Slides 21-35)
- K-Fold, Stratified, and Grouped Cross-Validation.
- Nested CV for simultaneous tuning and evaluation.
- Metrics for Reliability: Beyond ^2$ (e.g., Mean Absolute Percentage Error, uncertainty calibration).

### Part 4: Regularization & Shrinkage (Slides 36-45)
- L2 Regularization (Ridge): Keeping weights small.
- L1 Regularization (Lasso): Feature selection through sparsity.
- Early Stopping: The most powerful regularization for NNs.

### Part 5: Mapping Process Windows (Slides 46-50)
- Using ML to find "Safe" zones in Processing space.
- Sensitivity analysis: Which parameter "breaks" the process first?
- Case Study: Process stability in Casting or 3D Printing.

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 8:**  
This unit shifts the focus from model performance to **Model Reliability**. We explore the Bias-Variance tradeoff and the fundamental challenge of generalization—ensuring that an ML model works on new, unseen data from the factory floor. We introduce robust validation techniques like K-Fold and Stratified Cross-Validation to stabilize performance estimates on small materials datasets. A key focus is on **Process Robustness**, where we use sensitivity analysis to identify "Process Windows"—regions in parameter space where material quality is maximized and insensitive to industrial noise.
