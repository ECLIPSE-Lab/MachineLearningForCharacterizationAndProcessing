# Week 13 Summary: Physics-informed and constrained ML

## Cross-Book Summary

### 1. Physics-Informed Neural Networks (PINNs)
- **Embedding Laws:** Enforce ODEs/PDEs via the loss function for physical consistency.
- **Automatic Differentiation:** Exact derivative calculations enable NNs to evaluate physical equations.
- **Boundary Conditions:** Methods like Lagaris substitution guarantee boundary compliance.

### 2. Governing Equation Discovery
- **Dictionary-Based Regression:** Build a dictionary of candidate math functions.
- **Sparse Identification:** Use regularized regression (Lasso) to discover physical laws from noisy data.
- **Dimensional Reasoning:** Unit analysis ensures physically plausible discoveries.

### 3. Constraints in Materials Science
- **Monotonicity:** Enforce required physical trends (e.g., hardness vs. alloying).
- **Hybrid Modeling:** Combine physical "White-Box" models with data-driven "Black-Boxes" (Grey-Box).

## 90-Minute Lecture Strategy

### Part 1: Why Physics Matters
- Limits of unconstrained Black-Box models.
- Accurate but Physical models.
- PINNs need less data.

### Part 2: Automatic Differentiation
- GradientTape mechanics.
- Derivatives as ML architecture components.

### Part 3: Solving Physics with NNs
- PINN Architectures: Data Loss + Physics Loss.
- Enforcing Boundary Conditions.
- 3D printing heat transfer case study.

### Part 4: Equation Discovery
- Sparse Regression and candidate dictionaries.
- Damped pendulum equation case study.
- Unit Analysis search pruning.

### Part 5: The Grey-Box Future
- Hybrid architectures vs. FEA.
- Building industrial trust.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 13:**  
- Combines neural networks with physical laws via Physics-Informed ML.
- Introduces PINNs and automatic differentiation.
- Details Governing Equation Discovery using sparse regression.
- Applies physical constraints to build data-efficient Grey-Box models.