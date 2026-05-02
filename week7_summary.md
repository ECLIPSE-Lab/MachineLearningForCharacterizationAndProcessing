# Week 7 Summary: Time-series and process monitoring

## Cross-Book Summary

### 1. Sequential Data & Memory
- **Temporal Dimension:** Process logs are sequential; order matters.
- **RNNs:** Possess hidden states that act as memory.
- **Vanishing Gradients:** Basic RNNs struggle with long-term dependencies.
- **LSTMs/GRUs:** Use gates to selectively remember/forget information.

### 2. Materials Process Monitoring
- **Preprocessing:** Smoothing and "Triggering" to extract cycles.
- **Anomaly Detection:** Large prediction deviations signal defects.
- **Surrogate Models:** Fast RNN/LSTM replacements for slow simulations.

## 90-Minute Lecture Strategy

### Part 1: Processing as Sequence
- Time-dependency of microstructure.
- Sensor types (1D vs. logs).
- Event vs. Continuous.

### Part 2: Preprocessing
- Denoising filters.
- Triggering cycles.
- Temporal Feature Engineering.

### Part 3: RNNs
- Unrolled RNN structure.
- Vanishing Gradient problem.
- LSTM and GRU mechanics.

### Part 4: Case Studies
- Predictive Maintenance.
- AM melt pool stability.
- Dilatometry phase predictions.

### Part 5: Challenges
- Non-stationarity and machine drift.
- Transformers for 1D data.
- Closed-loop control outlook.

## Quarto Website Update (Summary)
**Summary for ML-PC Week 7:**  
- Applies ML to Time-Series Data for process monitoring.
- Introduces RNNs and LSTMs for sequential dependencies.
- Details essential preprocessing like smoothing and triggering.
- Covers anomaly detection and process outcome prediction.