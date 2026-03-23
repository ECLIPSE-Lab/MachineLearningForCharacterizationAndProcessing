# Week 12 Summary: Uncertainty-aware regression & Gaussian Processes

## Cross-Book Summary

### 1. The Value of "Knowing what you don't know" (Neuer Ch 6, Murphy Ch 15)
- **Epistemic vs. Aleatoric Uncertainty:** 
  - **Aleatoric:** The inherent randomness in the physical process (e.g., sensor noise).
  - **Epistemic:** The model's ignorance due to lack of training data in a specific region of the parameter space.
- **Danger of Overconfidence:** Standard neural networks often provide "point estimates" that can be wildly overconfident when extrapolating into unknown physical regimes.

### 2. Gaussian Processes (GPs) (Murphy Ch 15, Bishop Ch 6)
- **Distribution over Functions:** A GP defines a prior over an infinite space of functions. After seeing data, it provides a posterior distribution, yielding both a mean prediction and a variance (uncertainty).
- **Kernels as Physical Priors:** The kernel function (e.g., Radial Basis Function or Matérn) encodes our assumptions about the smoothness and length scales of the physical phenomenon (Bishop Ch 6.4).
- **Non-Parametric Nature:** Unlike NNs, GPs don't have a fixed number of parameters; they scale with the number of training points, making them ideal for "small but high-quality" materials datasets.

### 3. GP-Based Process Maps (ML-PC Index)
- **Confidence Ribbons:** Visualizing the uncertainty allows engineers to see where a process map is reliable and where more experiments are needed.
- **Kriging:** GP regression is closely related to Kriging, a method long used in geostatistics and now widely applied to interpolate materials property surfaces.

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: Uncertainty in Science (Slides 1-10)
- Why a single number is never enough.
- Risk management in materials processing: The cost of being wrong.
- Visualizing distributions: Histograms, error bars, and density plots.

### Part 2: Gaussian Process Fundamentals (Slides 11-25)
- The Bayesian viewpoint: Function space vs. Parameter space.
- Kernels: How do we define "Similarity" between two material states?
- The GP Math: Conditional Gaussians and Matrix Inversion.
- Interpreting the Variance: Where does the "Shaded region" come from?

### Part 3: GP Case Studies (Slides 26-40)
- Case Study: Predicting tensile strength across a temperature-strain rate space.
- GP for Experimental Design: Identifying the "Gaps" in a database.
- Multi-Task GPs: Sharing information between related properties (e.g., Hardness and Yield Strength).

### Part 4: Advanced Probabilistic ML (Slides 41-45)
- Mixture Density Networks (MDNs): Handling multi-modal uncertainties (Neuer Ch 6.4).
- Dropout as a Bayesian approximation in deep NNs.

### Part 5: Summary: Decision Making Under Uncertainty (Slides 46-50)
- Using confidence intervals to define "Safe" process windows.
- Summary: Building models that scientists can trust.

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 12:**  
This unit introduces **Probabilistic Machine Learning**, focusing on the quantification of uncertainty in materials models. We explore why point estimates can be dangerous in engineering and introduce **Gaussian Processes (GPs)** as a powerful tool for uncertainty-aware regression. Students learn how kernels encode physical assumptions about data smoothness and how the resulting predictive distributions can be used to build robust process maps. We also discuss the difference between aleatoric (noise) and epistemic (ignorance) uncertainty and how to use confidence intervals to drive scientific decision-making.
