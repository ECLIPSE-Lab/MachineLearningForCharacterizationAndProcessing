# Week 6 Summary: Data scarcity & transfer learning

## Cross-Book Summary

### 1. The Small Data Challenge (Sandfeld Ch 11, Neuer Ch 4)
- **Experimental Cost:** Unlike internet-scale data, scientific datasets are expensive. A model with millions of parameters (like a CNN) will easily "memorize" a small materials dataset rather than learning the underlying physics.
- **Generalization:** To avoid overfitting, we must use techniques like early stopping, dropout, and robust train/val/test splitting (Neuer Ch 4.2.1).

### 2. Transfer Learning (McClarren Ch 6, Sandfeld Ch 19)
- **Leveraging Pretrained Models:** Instead of training from scratch, we start with a model (e.g., ResNet, EfficientNet) trained on massive datasets like ImageNet.
- **Feature Reuse:** The "early" layers of a CNN learn universal visual primitives (edges, blobs, textures) that are surprisingly effective for micrographs, even if the model was originally trained on natural objects like dogs or cars.
- **Fine-Tuning Strategies:** 
  - **Feature Extraction:** Freeze the backbone and train only the final classification head.
  - **Fine-Tuning:** Unfreeze the last few convolutional blocks and train with a very low learning rate.
- **Case Study (McClarren):** Transferring EfficientNet features to detect volcanoes on Venus—a scientific task with limited labeled data.

### 3. Data Augmentation
- **Artificial Scarcity Relief:** Increasing the effective dataset size by applying transformations: rotation, flipping, cropping, and color jittering.
- **Physics-Preserving Augmentation:** In materials science, rotations and flips often preserve the underlying physical meaning (unless there is a macro-scale gradient or oriented growth), unlike in natural images where "upside-down" objects are rare.

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: The Curse of Small Data (Slides 1-10)
- Why materials data is "Small, Expensive, and Messy."
- The risk of overfitting: When your model learns the specific scratches on a sample instead of the phase boundaries.

### Part 2: Fighting Scarcity with Augmentation (Slides 11-20)
- Traditional Augmentation: Flips, Rotations, Zooms.
- Advanced Augmentation: Mixup, Cutmix.
- Domain-specific Augmentation: Adding simulated noise or artifacts.

### Part 3: Transfer Learning Mechanics (Slides 21-35)
- The concept of "Feature Hierarchies."
- Pretrained Models: An overview of available backbones.
- How to implement Transfer Learning: Freezing, Unfreezing, and Learning Rates.
- Case Study: ImageNet to SEM images.

### Part 4: Domain Shift in Science (Slides 36-45)
- Does ImageNet pretraining always help? (Comparing natural vs. scientific domains).
- Cross-Material Transfer: Training on Steel and fine-tuning on Aluminum.
- Synthetic-to-Real Transfer: Pretraining on simulations (Phase Field, FEM).

### Part 5: Summary & Best Practices (Slides 46-50)
- Selecting the right backbone.
- Validation strategies for small data.
- Discussion: Is "Learning to Learn" the future of Materials Science?

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 6:**  
This unit addresses the fundamental bottleneck of materials informatics: **Data Scarcity**. We explore how to build powerful deep learning models when only a few hundred labeled images or signals are available. The core focus is on **Transfer Learning**, where we leverage knowledge from models pretrained on millions of natural images to accelerate learning and improve generalization on materials tasks. We also cover **Data Augmentation** strategies tailored for scientific data and discuss when and why transferring knowledge across different physical domains succeeds or fails.
