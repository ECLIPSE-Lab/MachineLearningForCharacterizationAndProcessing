# Week 13 Summary: Physics-informed and constrained ML

## Cross-Book Summary

### 1. Physics-Informed Neural Networks (PINNs) (Neuer Ch 6)
- **Embedding Laws:** Instead of letting a network learn purely from data, we enforce physical laws (ODEs, PDEs) by including them in the loss function. This ensures the model's predictions are physically consistent (e.g., mass or energy is conserved).
- **Automatic Differentiation:** Modern deep learning frameworks (Tensorflow, PyTorch) allow for the exact calculation of derivatives of the network's output with respect to its inputs. This enables the network to "evaluate" physical equations during the training process (Neuer Ch 6.3.1).
- **Boundary Conditions:** Techniques like the Lagaris substitution allow us to force the network to satisfy initial or boundary conditions by design, rather than just as a soft constraint in the loss function (Neuer Ch 6.3.3).

### 2. Governing Equation Discovery (McClarren Ch 2.5)
- **Dictionary-Based Regression:** If we don't know the exact law but suspect its form, we can build a "dictionary" of candidate functions (e.g., $\sin \theta, \theta^2, \dot{\theta}$). 
- **Sparse Identification:** Using regularized regression (Lasso), we can identify which few terms from the dictionary are actually responsible for the observed behavior, effectively "discovering" the underlying physics from noisy experimental data.
- **Dimensional Reasoning:** Using unit analysis to guide the search for coefficients, ensuring the discovered model is physically plausible (McClarren Ch 2.5.1).

### 3. Constraints in Materials Science (ML-PC Index)
- **Monotonicity:** Ensuring that a predicted property (e.g., hardness) always increases with a specific alloying element if the physics demands it.
- **Hybrid Modeling:** Combining a physical "White-Box" model for well-understood parts of a process with a data-driven "Black-Box" for the complex, unknown parts (Grey-Box modeling).

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: Why Physics Matters in ML (Slides 1-10)
- The limits of unconstrained "Black-Box" models.
- "Accurate but Physical": Why we need models that respect conservation laws.
- The cost of training: PINNs require significantly less data.

### Part 2: Automatic Differentiation (Slides 11-20)
- The fundamental engine: How GradientTape works (Neuer Ch 6.3).
- Derivatives as first-class citizens in ML architectures.
- Practical Example: Implementing a simple derivative constraint in code.

### Part 3: Solving Physics with NNs (Slides 21-35)
- PINN Architectures: The Data Loss + The Physics Loss.
- Enforcing Boundary and Initial Conditions (The Lagaris Approach).
- Case Study: Heat transfer in 3D printing (solving the Heat Equation).

### Part 4: Equation Discovery from Lab Data (Slides 36-45)
- Sparse Regression and the "Dictionary of Laws."
- Case Study: Discovering the damped pendulum equation (McClarren Ch 2.5).
- Using Unit Analysis to prune the search space.

### Part 5: Summary: The Grey-Box Future (Slides 46-50)
- Hybrid architectures: When to use PINNs vs. traditional FEA.
- Building trust: Why physical models are easier to deploy in industry.
- Summary: ML as a partner to physical intuition.

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 13:**  
This unit explores **Physics-Informed Machine Learning**, a paradigm that combines the flexibility of neural networks with the rigor of physical laws. We introduce **Physics-Informed Neural Networks (PINNs)** and discuss how automatic differentiation allows us to embed ordinary and partial differential equations directly into the training process. We also explore **Governing Equation Discovery**, using sparse regression to "extract" physical laws from noisy experimental data. Students learn how to apply physical constraints like monotonicity and conservation to build hybrid models that are more data-efficient, interpretable, and trustworthy for materials engineering.
