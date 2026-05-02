# Week 6 Summary: Data scarcity & transfer learning

## Cross-Book Summary

### 1. The Small Data Challenge
- **Cost:** Scientific data is expensive; deep networks easily overfit small datasets.
- **Generalization:** Requires early stopping, dropout, and robust splits to avoid overfitting.

### 2. Transfer Learning
- **Pretrained Models:** Start with models trained on massive datasets (e.g., ImageNet).
- **Feature Reuse:** Early layers learn universal visual primitives useful for micrographs.
- **Fine-Tuning:** Freeze backbone and train the head, or unfreeze late layers with a low learning rate.

### 3. Data Augmentation
- **Artificial Relief:** Expand data via rotation, flipping, cropping, etc.
- **Physics-Preserving:** Materials rotations/flips preserve physical meaning.

## 90-Minute Lecture Strategy

### Part 1: Curse of Small Data
- Small, Expensive, Messy data.
- Overfitting risks.

### Part 2: Augmentation
- Traditional: Flips, Rotations.
- Advanced: Mixup, Cutmix.
- Domain-specific: Simulated noise.

### Part 3: Transfer Learning Mechanics
- Feature Hierarchies.
- Available backbones.
- Fine-tuning strategies.

### Part 4: Domain Shift in Science
- Natural vs. scientific domains.
- Cross-Material Transfer.
- Synthetic-to-Real Transfer.

### Part 5: Summary & Best Practices
- Backbone selection.
- Small data validation.
- "Learning to Learn".

## Quarto Website Update (Summary)
**Summary for ML-PC Week 6:**  
- Addresses Data Scarcity in materials informatics.
- Explores Transfer Learning to leverage pretrained models.
- Discusses scientific Data Augmentation strategies.
- Evaluates cross-domain knowledge transfer limits.