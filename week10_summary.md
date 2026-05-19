# Week 10 Summary: Transformers for materials characterization

## Cross-Book Summary

### 1. Why Attention for Materials
- **Long-range correlations:** Many characterization signals (diffraction, micrograph stacks) have dependencies that exceed practical CNN receptive fields.
- **Self-attention:** Lets every token attend to every other token directly, capturing global structure in one layer.

### 2. The Transformer Toolkit
- **Scaled dot-product attention:** The core operation and its O(L²) cost.
- **Vision Transformer (ViT):** Patchify → embed → encode → classify; transformers applied to image-like data.
- **Flash Attention:** A fused kernel that makes long sequences tractable without materialising the L×L matrix.

### 3. Materials Applications
- **ViT on 4D-STEM:** Diffraction patches become a token sequence for a ViT encoder.
- **Cross-attention across LPBF layers:** Long-stack micrograph context for additive-manufacturing monitoring.

### 4. Scaling Alternatives (Awareness Only)
- **Mamba / structured state-space models (SSMs):** O(L) compute, constant memory; competitive on long sequences. Cross-reference the Week 7 time-series deck.

## 90-Minute Lecture Strategy

### Part 1: Where We Are
- Recap of Week 9 (characterization signals) and why we now need attention.

### Part 2: Why Attention
- Long-range correlations exceed CNN receptive fields.

### Part 3: Mechanics
- Scaled dot-product attention: the formula and the cost.
- ViT in five lines: patchify, embed, encode, classify.
- Flash Attention: the kernel that makes long sequences tractable.

### Part 4: Materials Applications
- ViT on 4D-STEM diffraction.
- Cross-attention across LPBF layer stacks.

### Part 5: Practice and Pitfalls
- `nn.MultiheadAttention` vs `F.scaled_dot_product_attention`.
- Scaling alternatives (Mamba / SSMs) — mention only.
- Anti-patterns: what *not* to do.
- Exercise preview.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 10:**
- Motivates self-attention for long-range structure in characterization data.
- Covers scaled dot-product attention, the Vision Transformer, and Flash Attention.
- Applies transformers to 4D-STEM diffraction and LPBF layer-stack context.
- Notes Mamba / state-space models as scaling alternatives, and when not to reach for a transformer.
