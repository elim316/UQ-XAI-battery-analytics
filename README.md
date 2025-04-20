# Uncertainty & Explainability in Battery Management AI Systems

![Research Project](https://img.shields.io/badge/Project-Research-blue)
![Focus](https://img.shields.io/badge/Focus-Explainable%20AI%20%7C%20Uncertainty%20Quantification-purple)
![Domain](https://img.shields.io/badge/Domain-Battery%20Analytics-orange)
![Built With](https://img.shields.io/badge/Built%20With-Python-yellow)
![Models](https://img.shields.io/badge/Model-CNN-lightblue)
![Explainability](https://img.shields.io/badge/XAI-Techniques%3A%20SHAP%20%7C%20LIME-green)
![Calibration](https://img.shields.io/badge/Calibration-ACI%20%7C%20PICP%20%7C%20ECE-red)

---

## Overview

This project explores the application of **uncertainty quantification (UQ)** and **explainable AI (XAI)** to deep learning models used in **battery state-of-health (SOH) estimation**. The system is part of a **cognitive digital twin** for advanced battery analytics.

---

## Objectives

- Quantify **model and data uncertainty** in battery health predictions
- Implement and evaluate **explainability techniques** for CNN predictions
- Ensure traceability and reliability of model outputs in **real-time battery management systems**
- Evaluate robustness and generalisability across multiple datasets

---

## Techniques & Frameworks

### Explainability (XAI)
- SHAP
- LIME
- Integrated Gradients
- Counterfactual Explanations

Evaluated across:  
- Fidelity (MAE)  
- Consistency (R²)  
- Stability (Counterfactual Validity)

✅ **SHAP** showed the most robust and interpretable results.

---

### Uncertainty Quantification

- **Monte Carlo Dropout** for model uncertainty  
- **Gaussian noise injection** for data uncertainty  
- **Adaptive Confidence Intervals (ACI)** to combine both sources
- **Predictive Certainty Ranges**, **MPIW**, and under/overconfidence analysis

#### Calibration Metrics:
- ECE
- MCE
- PICP

---

## Datasets Used

- **Oxford Battery Dataset**
- **McMaster Battery Dataset**  
Trained on McMaster, tested on Oxford for generalisability.

---

## My Contributions

- Built CNN architecture for SOH estimation
- Integrated 4 XAI methods with post-hoc evaluation pipeline
- Designed the **Adaptive Confidence Interval** (ACI) framework
- Implemented ECE, MCE, and PICP metrics for uncertainty evaluation
- Designed a **Streamlit-based interface** to visualise predictions, explanations, and confidence bands
- Conducted comparative analysis of explainability tools and uncertainty calibration methods

---

## What I Learned

- Real-world application of explainability techniques in battery health analytics
- Building models with **quantified trust** — beyond accuracy
- Combining probabilistic reasoning with deep learning predictions
- Evaluating model generalisability under noisy/shifted data conditions

---

## Note

Due to the nature of the research collaboration, source code and raw datasets may not be publicly available. This case study serves to document methodology and technical contributions.

---
