# Week 5 Summary: Unsupervised Learning in Materials

## Cross-Book Summary

### 1. The Need for Convolutions (McClarren Ch 6)
- **The Parameter Explosion:** A standard Multi-Layer Perceptron (MLP) treating every pixel as an independent input requires a massive number of weights, making it prone to overfitting and computationally expensive.
- **Exploiting Structure:** Images have spatial correlation (neighboring pixels are related). Convolutions take advantage of this by applying the same small "filter" across the entire image (Weight Sharing).
- **Shift Invariance:** A crack or a pore should be recognized regardless of where it appears in the micrograph.

### 2. CNN Mechanics (McClarren Ch 6, Sandfeld Ch 17)
- **Convolutional Layers:** These act as feature detectors. Early layers might detect simple edges, while deeper layers detect complex morphologies (e.g., dendrites, lath martensite).
- **Activation & Pooling:** Non-linear activations (ReLU) allow the network to learn complex patterns. Pooling layers (Max/Avg) downsample the feature maps, providing spatial robustness and reducing computation.
- **The Perception Analogy:** Modern CNNs are distant descendants of the Rosenblatt Perceptron, which was originally inspired by the Cadmium Sulfide photo-cells used to "perceive" simple pixel grids (Sandfeld Ch 17.2).

### 3. Application to Microstructures (ML-PC Index)
- **Segmentation:** Assigning a class (e.g., α-phase, β-phase) to every pixel.
- **Object Detection:** Finding and bounding specific features (e.g., precipitates, micro-cracks).
- **Classification:** Categorizing an entire micrograph (e.g., "Good" vs. "Defective" process outcome).

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: Applied Clustering (45 mins)
- *Case Study 1:* Automated phase segmentation in EDS/EDX maps using K-Means and GMMs.
- *Case Study 2:* Anomaly/defect detection in acoustic or thermal sensor streams during manufacturing.

### Part 2: Applied Autoencoders (45 mins)
- *Case Study 1:* Convolutional Autoencoders (CAEs) to compress high-dimensional microstructures (like 3D X-ray Tomography volumes).
- *Case Study 2:* Exploring the latent space to automatically discover categories of defects or structural motifs without human supervision.

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 5:**
This unit transitions from supervised networks to **Unsupervised Learning** in materials characterization. By applying clustering algorithms (K-Means, GMMs) and Autoencoders, we tackle the "unlabeled data" problem pervasive in materials science. Through case studies in EDS map segmentation, defect detection in sensor streams, and latent space exploration of 3D microstructures, students learn how to autonomously discover structural motifs and reduce dimensionality without requiring manual annotations.
