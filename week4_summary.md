# Week 4 Summary: From classical microstructure metrics to learned representations

## Cross-Book Summary

### 1. Classical Microstructure Metrics (Sandfeld, Domain Knowledge)
- **Stereology:** The traditional method of quantifying 3D structure from 2D sections (e.g., grain size, phase fractions).
- **Hand-crafted Descriptors:** Features like aspect ratio, tortuosity, and circularity. These are physically interpretable but biased by human intuition.
- **The Information Bottleneck:** By reducing a complex micrograph to a few scalar metrics (like "average grain size"), we may discard the very information responsible for rare failure events or subtle property changes.

### 2. The Foundation of Learned Representations (Neuer Ch 4.5, McClarren Ch 8, Bishop Ch 5)
- **The Artificial Neuron:** A mathematical unit that performs a weighted sum of inputs ($ \text{net} = \sum w_i x_i + b $) followed by a non-linear activation function.
- **Activation Functions:** ReLU, Sigmoid, and Tanh introduce the non-linearity required to approximate complex structure-property mappings. ReLU is the current standard for deep learning (Sandfeld Ch 18).
- **Universal Approximation:** A network with even one hidden layer can approximate any continuous function, allowing it to "learn" a representation of the data that is optimal for a given task.
- **MLP Topology:** Multi-Layer Perceptrons stack these neurons to create increasingly abstract representations of the input data.

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: The Classical Approach (Slides 1-15)
- How we currently describe materials: Grain size, phase fractions, orientation maps.
- Quantitative Metallography: Methods and standards.
- Successes and failures of hand-crafted features.

### Part 2: Feature Engineering vs. Feature Learning (Slides 16-25)
- The concept of a "Representation."
- Why "expert" features might be incomplete.
- The shift from "calculating metrics" to "learning embeddings."

### Part 3: The Building Blocks of ML (Slides 26-40)
- The Mathematical Neuron (Neuer Ch 4.5.1).
- Weights and Biases: The "knobs" of the model.
- Activation Functions: Why we need non-linearity (ReLU, Sigmoid).
- Forward propagation: From input data to prediction.

### Part 4: Multi-Layer Perceptrons (MLP) (Slides 41-45)
- Stacking layers to build abstraction.
- The concept of "Hidden" layers.
- Neural networks as universal function approximators.

### Part 5: Outlook: Learning from Microstructures (Slides 46-50)
- Preview of Week 5: Moving from vectors to images (CNNs).
- Discussion: Can we trust a "Learned" metric more than an ASTM grain size?

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 4:**  
This unit marks the transition from classical, hand-crafted microstructure quantification (like grain size and phase fractions) to the modern paradigm of **learned representations**. We first review traditional stereological metrics and their limitations in capturing complex structural nuances. We then introduce the foundational unit of modern ML: the **artificial neuron**. By understanding weights, biases, and non-linear activation functions, we build the framework for Multi-Layer Perceptrons (MLPs) that can automatically learn optimal features from materials data.
