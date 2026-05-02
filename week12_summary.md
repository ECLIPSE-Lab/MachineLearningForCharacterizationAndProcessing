# Week 12 Summary: Uncertainty-aware regression & Gaussian Processes

## Cross-Book Summary

### 1. Knowing what you don't know
- **Aleatoric vs. Epistemic:** Inherent physical noise vs. model ignorance.
- **Overconfidence Danger:** Point estimates fail safely in unknown regimes; uncertainty metrics are crucial.

### 2. Gaussian Processes (GPs)
- **Distribution over Functions:** GP yields posterior mean and variance (uncertainty).
- **Kernels as Physical Priors:** Encodes assumptions about data smoothness/scale.
- **Non-Parametric Nature:** Scales with data size, ideal for small, high-quality materials datasets.

### 3. GP-Based Process Maps
- **Confidence Ribbons:** Visualize reliability to guide further experiments.
- **Kriging:** Interpolates materials property surfaces using GP regression.

## 90-Minute Lecture Strategy

### Part 1: Uncertainty in Science
- Risk management in materials processing.
- Visualizing distributions and error bars.

### Part 2: GP Fundamentals
- Function vs. Parameter space.
- Kernels and "Similarity".
- Conditional Gaussians and Variance.

### Part 3: GP Case Studies
- Predicting tensile strength across parameters.
- GP for Experimental Design.
- Multi-Task GPs.

### Part 4: Advanced Probabilistic ML
- Mixture Density Networks (MDNs).
- Dropout as Bayesian approximation.

### Part 5: Decision Making
- Safe process windows via confidence intervals.
- Building trustworthy models.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 12:**  
- Introduces Probabilistic Machine Learning for uncertainty quantification.
- Differentiates aleatoric (noise) from epistemic (ignorance) uncertainty.
- Uses Gaussian Processes (GPs) for uncertainty-aware regression.
- Applies confidence intervals to map robust process windows.