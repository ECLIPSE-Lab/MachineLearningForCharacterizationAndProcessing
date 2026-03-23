# Week 2 Summary: Physics of data formation

## Cross-Book Summary

### 1. Signal Formation & Noise (Neuer, Sandfeld)
- **Measurement as a Mapping:** Every characterization signal is a convolution of the true physical state with the instrument's point spread function (PSF).
- **Stochastics of Data:** Data should be viewed as a stochastic process (Neuer Ch 2). Probabilities (Laplace definition) and sets help formalize the occurrence of events in discrete measurements (Sandfeld Ch 5).
- **Noise as a Physical Prior:** Noise is not just a nuisance to be removed; its distribution (Poisson for shot noise, Gaussian for thermal) tells us about the physics of the detector.

### 2. Dimension Reduction & Structure (McClarren, Neuer, Bishop)
- **The Curse of Dimensionality:** Experimental data often has high dimensionality (thousands of pixels or spectral channels) but low intrinsic rank.
- **SVD vs. PCA:**
  - PCA (Principal Component Analysis) focuses on the covariance matrix (Neuer Ch 5.2).
  - SVD (Singular Value Decomposition) is the matrix factorization ($\mathbf{X} = \mathbf{U} \mathbf{S} \mathbf{V}^T$) used to compute it efficiently (McClarren Ch 4).
- **Principal Variations:** The first few singular vectors capture the most significant "modes" of variation. In materials science, these correspond to physical phenomena (e.g., primary grain orientations or dominant chemical shifts).
- **Reduced Order Modeling (ROM):** PCA allows us to represent complex time-series or images with a few "scores" ({i1}, u_{i2}$), which can then be mapped to processing parameters via regression (McClarren example).

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: The Measurement Chain (Slides 1-10)
- From atoms to bits: The signal formation process.
- Resolution, Contrast, and Information depth.
- Sampling and Aliasing: The Nyquist-Shannon limit in the lab.

### Part 2: Statistical Foundations (Slides 11-20)
- Review of Variance, Covariance, and Correlation (Neuer Ch 2).
- The Covariance Matrix: A geometric view of data spread.
- Noise distributions: Why your error bars look the way they do.

### Part 3: Dimensionality Reduction: PCA/SVD (Slides 21-35)
- The intuition: Finding the "Natural" coordinate system of the data.
- Step-by-step PCA: Mean centering, Covariance, Eigen-decomposition.
- SVD: The engine of dimension reduction.
- Interpreting Singular Values: The "Scree Plot" and explained variance.

### Part 4: Materials Case Studies (Slides 36-45)
- Spectral Denoising: Using PCA to separate signal from noise in EDS/XRD.
- Time-series Compression: Managing high-frequency process logs.
- Microstructure Eigen-modes: What does the "average" grain look like?

### Part 5: Physics-ML Integration (Slides 46-50)
- PCA as a "Physical Mode Finder."
- When PCA fails: Non-linearity and the need for more complex manifolds.
- Introduction to the Fourier exercise: Inspecting periodicity in micrographs.

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 2:**  
This unit bridges the gap between the physical process of data acquisition and the mathematical tools used to describe it. We analyze how signals are formed in characterization tools and how physical constraints (resolution, noise, sampling) act as priors for learning. We then introduce Principal Component Analysis (PCA) and Singular Value Decomposition (SVD) as fundamental techniques for discovering low-dimensional structure in high-dimensional experimental datasets.
