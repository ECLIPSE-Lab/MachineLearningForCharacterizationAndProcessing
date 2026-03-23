# Week 9 Summary: Inverse problems and process maps

## Cross-Book Summary

### 1. Forward vs. Inverse Problems (Bishop Ch 5, Neuer Ch 6)
- **The Causality Gap:** Forward problems (Process → Structure) usually have a unique solution driven by causality. Inverse problems (Structure → Process) are often "ill-posed" or multi-valued, meaning different processing paths can lead to identical microstructures (Bishop Ch 5.18).
- **Non-Gaussianity:** Standard least-squares regression assumes a Gaussian distribution of targets. In inverse problems, the distribution can be multimodal, requiring more advanced techniques like Mixture Density Networks (Bishop Ch 5.19).

### 2. Physics-Informed Enrichment (Neuer Ch 6)
- **The "Expert in the Loop" Principle:** Why hide physical laws from the algorithm? By providing physical transformations (e.g., Fourier Transform for oscillating signals or dimensionless numbers), we reduce the training effort and make the model more interpretable.
- **Enrichment:** Adding transformed features alongside raw data creates a "Physics-Informed Neural Network" (PINN) that leverages both data and laws (Neuer Ch 6.1).

### 3. Process Maps and Corridors (Neuer Ch 6.4, ML-PC Index)
- **Process Corridors:** Identifying the stable regions in parameter space where the desired material properties are consistently achieved.
- **ML-Guided Mapping:** Using surrogates to interpolate between sparse experimental points, allowing for the rapid visualization of complex process maps (e.g., AM laser power vs. scan speed).
- **Prescriptive ML:** Shifting from "What will happen?" to "What must I do to achieve this property?"

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: The Material Scientist's Dilemma (Slides 1-10)
- Why the inverse problem is the "Real" problem in R&D.
- Structure-to-Process: The difficulty of many-to-one mappings.
- The Concept of "Uniqueness" in physical systems.

### Part 2: Physics-Informed ML (Slides 11-20)
- White-Box vs. Black-Box vs. Grey-Box (Neuer Ch 6).
- Feature Enrichment: Helping the network "see" the physics (e.g., FFT).
- Embedding constraints in the Loss Function.

### Part 3: Solving the Inverse (Slides 21-35)
- The failure of standard regression on inverse tasks (Bishop Ch 5.19).
- Approaches to ill-posed problems: Regularization, Bayesian Inference, and Mixture Models.
- Case Study: Determining heat treatment parameters from grain size distributions.

### Part 4: Building Process Maps (Slides 36-45)
- From experimental points to continuous maps.
- Visualizing Process Windows and "Safe" Corridors.
- Case Study: High-throughput mapping of laser-material interactions.

### Part 5: Summary: ML for Material Design (Slides 46-50)
- Designing new processing routes with ML surrogates.
- The role of simulation in training inverse models.
- Reflection: Can ML truly replace human intuition in the lab?

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 9:**  
This unit explores **Inverse Problems**—the cornerstone of materials design where we seek the processing parameters required to achieve a target microstructure or performance. We contrast these with causal forward problems and discuss why they are often ill-posed and multi-valued. We introduce **Physics-Informed Learning** as a way to solve these challenges by enriching models with physical transformations and constraints. Students learn how to build and interpret **Process Maps** and "Process Corridors," using machine learning to visualize safe operating regions in complex experimental spaces.
