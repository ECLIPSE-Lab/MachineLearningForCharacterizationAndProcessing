# Week 10 Summary: ML for characterization signals

## Cross-Book Summary

### 1. Clustering Spectral Data
- **K-Means:** Groups similar spectra (XRD/EDS) to identify distinct phases.
- **Mini-Batch K-Means:** Speeds up high-throughput characterization.
- **t-SNE:** Projects high-dimensional spectra to 2D to reveal outliers/relationships.

### 2. Autoencoders for Signal Processing
- **Latent Representations:** Compresses spectra to essential physical information.
- **Denoising:** Reconstructs clean signals from noisy inputs without blurring.
- **Non-linear Compression:** Outperforms PCA for complex spectral libraries.

### 3. Scientific Integrity in ML
- **Peak Preservation:** ML must assist, not invent or smooth away real physics.

## 90-Minute Lecture Strategy

### Part 1: High-Dimensional Signals
- Digital footprint: XRD, EDS, EELS, Raman.
- Manual vs. automated peak-picking.
- Vector spectrum representation.

### Part 2: Clustering Structure
- K-Means algorithm.
- Elbow Method for phase counting.
- Ternary alloy mapping.

### Part 3: Visualizing the Unseen
- t-SNE Stochastic Proximity.
- Hidden relationships.
- t-SNE distance pitfalls.

### Part 4: Autoencoders & Denoising
- Encoder-Bottleneck-Decoder.
- Denoising characterization signals.
- Bottlenecks as physical descriptors.

### Part 5: Data to Discovery
- Real-time spectral analysis.
- Physical consistency in ML.
- Automated pipelines.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 10:**  
- Processes high-dimensional Characterization Signals (XRD, EDS).
- Employs K-Means and t-SNE for automated phase identification.
- Uses Autoencoders for latent space compression and denoising.
- Enhances high-throughput data analysis while preserving physics.