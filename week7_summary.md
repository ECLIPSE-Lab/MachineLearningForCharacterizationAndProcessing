# Week 7 Summary: Time-series and process monitoring

## Cross-Book Summary

### 1. Sequential Data & Memory (McClarren Ch 7, Bishop Ch 13)
- **The Temporal Dimension:** Unlike images or static property predictions, process data (temperature logs, laser power, rolling force) is a sequence where the order matters.
- **Recurrent Neural Networks (RNNs):** These networks have a "hidden state" that acts as a memory, carrying information from previous time steps to influence current predictions.
- **The Vanishing Gradient Problem:** Basic RNNs struggle with long-term dependencies because the gradient "fades" as it is back-propagated through time (McClarren Ch 7.1.1).
- **LSTMs and GRUs:** These gated architectures solve the memory problem by selectively "remembering" or "forgetting" information, allowing the model to focus on relevant historical events.

### 2. Materials Process Monitoring (ML-PC Index, Neuer Ch 3)
- **Preprocessing for Time-Series:** Signal smoothing (moving average) and **Triggering** are essential. Triggering involves cutting out repetitive cycles from a long continuous log to allow for a direct comparison of process "pulses" (Neuer Ch 3.5).
- **Anomaly Detection:** Using the history of a process to predict the next expected signal; a large deviation from this prediction indicates a process fault or material defect.
- **Surrogate Models for Processing:** Training RNNs/LSTMs as "Fast" surrogates for slow physical simulations of thermal histories or phase transformations.

---

## 90-Minute Lecture Strategy (50 Slides)

### Part 1: Processing as a Sequence (Slides 1-10)
- The time-dependency of microstructural evolution.
- Types of signals: 1D sensors (thermocouples) vs. high-frequency logs (melt pool monitoring).
- The "Event" vs. "Continuous" perspective.

### Part 2: Time-Series Preprocessing (Slides 11-20)
- Denoising: Moving average and Gaussian filters.
- Triggering: Extracting meaningful process cycles (Neuer Ch 3.5).
- Feature Engineering in the Time Domain: Slopes, peaks, and Fourier coefficients.

### Part 3: Recurrent Neural Networks (RNNs) (Slides 21-35)
- The Unrolled RNN: Connecting the past to the present.
- Why the "Gradient Vanishes": The mathematical bottleneck.
- LSTM (Long Short-Term Memory): Anatomy of a gate.
- GRU (Gated Recurrent Unit): A simplified alternative.

### Part 4: Case Studies: Process Monitoring (Slides 36-45)
- Predictive Maintenance for Motors (Neuer Ch 3 example).
- Melt pool stability in Additive Manufacturing.
- Predicting phase transformations from dilatometry curves.

### Part 5: Challenges & Future (Slides 46-50)
- The problem of non-stationarity: When the machine "drifts" over time.
- Beyond RNNs: A glimpse at Transformers for 1D data.
- Summary: From monitoring to closed-loop control.

---

## Quarto Website Update (Summary)
**Summary for ML-PC Week 7:**  
This unit explores the application of machine learning to **Time-Series Data**, specifically for monitoring and predicting materials processing outcomes. We introduce **Recurrent Neural Networks (RNNs)** and their advanced variants like **LSTMs**, which are designed to handle sequential dependencies. We discuss the critical preprocessing steps of signal smoothing and triggering required to handle noisy experimental logs. Through case studies in additive manufacturing and process stability, students learn how to build models that "remember" the processing history to predict future states and detect anomalies in real-time.
