# Week 9 Summary: Inverse problems and process maps

## Cross-Book Summary

### 1. Forward vs. Inverse Problems
- **Causality Gap:** Forward problems are unique; inverse are ill-posed/multi-valued.
- **Non-Gaussianity:** Inverse problems require Mixture Density Networks due to multimodality.

### 2. Physics-Informed Enrichment
- **Expert in the Loop:** Add physical transformations (e.g., FFT) to reduce training effort.
- **Enrichment:** Combine raw data with physics features (PINNs).

### 3. Process Maps and Corridors
- **Process Corridors:** Identifying stable parameter regions.
- **ML-Guided Mapping:** Interpolating sparse experimental points via surrogates.
- **Prescriptive ML:** Answering "What must I do?" instead of "What will happen?".

## 90-Minute Lecture Strategy

### Part 1: Material Scientist's Dilemma
- Inverse problem complexities.
- Many-to-one mappings.
- Uniqueness in systems.

### Part 2: Physics-Informed ML
- White vs. Grey vs. Black Box.
- Feature Enrichment.
- Loss function constraints.

### Part 3: Solving the Inverse
- Regression failure on inverse tasks.
- Regularization and Mixture Models.
- Heat treatment parameter case study.

### Part 4: Building Process Maps
- Continuous maps from points.
- Visualizing Safe Corridors.
- Laser-material interactions mapping.

### Part 5: ML for Material Design
- Prescribing processing routes.
- Simulation-aided training.
- AI vs. human intuition.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 9:**  
- Explores Inverse Problems for materials design.
- Contrasts multi-valued inverse tasks with causal forward problems.
- Introduces Physics-Informed Learning and feature enrichment.
- Demonstrates building Process Maps and Safe Corridors.