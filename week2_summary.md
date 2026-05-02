# Week 2 Summary: Physics of data formation

## Cross-Book Summary

### 1. Signal Formation & Noise
- **Measurement Mapping:** Signal = physical state convolved with instrument PSF.
- **Stochastics:** Data is a stochastic process.
- **Noise as Prior:** Noise distributions reveal detector physics.

### 2. Dimension Reduction & Structure
- **Dimensionality Curse:** High dimension, low intrinsic rank.
- **SVD vs. PCA:** PCA uses covariance; SVD factorizes matrix efficiently.
- **Principal Variations:** Top singular vectors capture main physical phenomena.
- **Reduced Order Modeling:** PCA scores map to processing parameters.

## 90-Minute Lecture Strategy

### Part 1: Measurement Chain
- Signal formation process.
- Resolution and Contrast.
- Nyquist-Shannon sampling limit.

### Part 2: Statistical Foundations
- Variance, Covariance, Correlation.
- Covariance Matrix geometry.
- Noise distributions.

### Part 3: Dimension Reduction
- Finding natural coordinates.
- PCA steps: Center, Covariance, Eigen-decomposition.
- SVD mechanics.
- Scree Plots and explained variance.

### Part 4: Materials Case Studies
- Spectral Denoising with PCA.
- Time-series Compression.
- Microstructure Eigen-modes.

### Part 5: Physics-ML Integration
- PCA as physical mode finder.
- Non-linear limits of PCA.
- Fourier periodicity exercise.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 2:**  
- Connects physical data acquisition to mathematical representation.
- Analyzes signal formation, resolution, and noise as priors.
- Introduces PCA and SVD for low-dimensional structure discovery.
- Demonstrates dimensionality reduction in high-dimensional datasets.