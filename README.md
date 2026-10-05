# Uncertainty Quantification and Explainable AI for Battery Analytics

Companion case study for the peer-reviewed paper published in IEEE Xplore: [Document 11249263](https://ieeexplore.ieee.org/document/11249263).

## Overview

This research applies uncertainty quantification (UQ) and post-hoc explainable AI (XAI) to convolutional neural networks (CNNs) used for lithium-ion battery state-of-health (SOH) estimation inside a cognitive digital twin pipeline.

In safety-critical battery management systems, point predictions alone are insufficient. Operators need calibrated confidence intervals alongside interpretable feature attributions to understand why a model predicts capacity degradation and how much trust to place in each estimate.

## Objectives

- Quantify both epistemic (model) and aleatoric (data) uncertainty in CNN state-of-health predictions.
- Compare post-hoc explainability methods on fidelity, consistency, and stability metrics.
- Evaluate cross-dataset generalisability by training on the McMaster Battery Dataset and testing on the Oxford Battery Dataset.

## Methodology

### Explainability (XAI)

Four attribution methods were integrated and benchmarked across Mean Absolute Error (fidelity), R-squared (consistency), and counterfactual validity (stability):

- SHAP (SHapley Additive exPlanations), which achieved the strongest stability and fidelity across degradation cycles
- LIME (Local Interpretable Model-agnostic Explanations)
- Integrated Gradients
- Counterfactual Explanations

### Uncertainty Quantification and Calibration

- Monte Carlo Dropout to capture epistemic model uncertainty
- Gaussian noise injection to model aleatoric sensor uncertainty
- Adaptive Conformal Inference (ACI) to construct calibrated prediction intervals combining both uncertainty sources
- Evaluated using Prediction Interval Coverage Probability (PICP), Mean Prediction Interval Width (MPIW), Expected Calibration Error (ECE), and Maximum Calibration Error (MCE)

## Key Contributions

- Designed the CNN architecture and training pipeline for battery state-of-health estimation.
- Implemented the Adaptive Conformal Inference (ACI) wrapper and calibration evaluators (ECE, MCE, PICP).
- Built the four-method XAI evaluation benchmark and a Streamlit visualiser to inspect degradation curves, feature attributions, and confidence bands interactively.

## Note on Data Availability

Because this work was conducted under a research collaboration, raw experimental datasets and proprietary model weights are not stored in this public repository. Please refer to the [IEEE Xplore publication](https://ieeexplore.ieee.org/document/11249263) for full experimental results and equations.
