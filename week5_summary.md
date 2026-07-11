# Week 5 Summary: Unsupervised Learning in Materials

## Cross-Book Summary

### 1. Learning Without Labels
- **Why Unsupervised:** Most materials data arrives unlabeled; labels are expensive.
- **Clustering:** K-Means and GMMs discover structure in descriptors and spectra.
- **Choosing K:** Cluster counts must be defensible, not arbitrary.

### 2. Embeddings and Autoencoders
- **Frozen CNN Embeddings:** Pretrained features as unsupervised feature spaces.
- **Autoencoders:** Bottleneck representations for compression and denoising.
- **Anomaly Detection:** Reconstruction-error thresholding on nominal data.

### 3. Application to Microstructures
- **Hyperspectral Clustering:** Flatten EELS/EDS datacubes, cluster, re-image as phase maps.
- **Phase Discovery:** Cluster CNN embeddings of micrographs without labels.
- **Defect Screening:** Flag off-nominal regions via autoencoder reconstruction error.

## 90-Minute Lecture Strategy

### Part 1: Applied Clustering
- Phase segmentation with K-Means/GMMs.
- Defect detection in sensor streams.

### Part 2: Applied Autoencoders
- CAE compression of 3D Tomography.
- Latent space defect discovery.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 5:**
- Shifts to Unsupervised Learning for unlabeled materials data.
- Covers clustering (K-Means, GMMs) and Autoencoders.
- Applies techniques to EDS segmentation and sensor anomaly detection.
- Explores 3D microstructure latent spaces for automated motif discovery.