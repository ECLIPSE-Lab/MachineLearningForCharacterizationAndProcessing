# Week 5 Summary: Neural networks for microstructure images

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

### Part 1: Why CNNs for Materials? (Slides 1-10)
- The failure of MLPs on image data.
- The concept of "Spatial Locality" in microstructures.
- The hierarchy of features: From pixels to phases.

### Part 2: The Convolutional Layer (Slides 11-25)
- Mathematical definition of 2D convolution.
- Filters in action: Edge detection (Sobel), Blurring (Gaussian).
- Hyperparameters: Stride, Padding, Filter Size.
- Weight Sharing and why it enables "Deep" learning.

### Part 3: Building a CNN (Slides 26-35)
- The Non-linear activation (ReLU) revisited.
- Pooling layers: Summarizing local information.
- The full stack: Conv -> Pool -> FC.

### Part 4: Case Studies: Microscopy (Slides 36-45)
- Automated Phase Fraction calculation using CNNs.
- Defect identification in CT or SEM images.
- Comparison: Fashion-MNIST (toy data) vs. Real Micrographs (experimental noise).

### Part 5: Challenges & Training (Slides 46-50)
- Data scarcity: The need for thousands of images.
- Overfitting: Why CNNs love to "memorize" your training set.
- Preview: How to handle "Small Data" (Week 6).

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 5:**  
This unit introduces **Convolutional Neural Networks (CNNs)**, the workhorse of modern computer vision, and applies them to materials characterization. We explore how convolutions allow networks to automatically learn hierarchical structure detectors—from simple edges to complex phase morphologies—while drastically reducing the number of parameters compared to standard MLPs. Through case studies in phase segmentation and defect detection, students learn the intuition behind filters, pooling, and the unique challenges of applying deep learning to high-resolution, noisy experimental micrographs.
