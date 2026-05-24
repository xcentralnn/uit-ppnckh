# UIT PPNCKH

## Improving Anomaly Detection Accuracy on Kubernetes Using Isolation Forest with Iterative Training and Data Balancing

This repository contains research materials for a UIT scientific research project on anomaly detection in Kubernetes environments.

The project focuses on improving a baseline Isolation Forest approach by combining:

- iterative multi-stage training to better handle concept drift,
- data balancing with SMOTE,
- robust feature scaling for heavy-tailed metrics,
- time-aware feature engineering,
- and optional integration of metrics and logs.

## Overview

Kubernetes is a standard platform for orchestrating containerized applications, but anomaly detection in real cluster environments remains challenging. Metrics data is often sparse, highly imbalanced, and changes over time as workloads evolve.

This project proposes a lightweight anomaly detection pipeline designed for practical Kubernetes monitoring. The goal is to improve detection quality while keeping inference fast enough for near real-time security and operations use cases.

## Objectives

1. Improve anomaly detection precision on Kubernetes metrics data.
2. Increase model robustness under changing workloads and concept drift.
3. Maintain practical runtime performance for real-world deployment.

## Proposed Method

The research pipeline is centered on Isolation Forest and includes:

1. Data collection from Prometheus metrics and Kubernetes event logs.
2. Preprocessing with missing-value handling and `RobustScaler`.
3. Data balancing with SMOTE to reduce severe class imbalance.
4. Time-based data splitting using a train-on-past, test-on-future strategy.
5. Iterative training and evaluation across multiple stages to refine the model.
6. Final comparison against a baseline Isolation Forest workflow.

## Expected Outcomes

- Precision above `92%`
- F1-score of at least `0.86`
- Inference latency below `15 ms/request`
- A reproducible experimental workflow for Kubernetes anomaly detection

## Repository Contents

This repository currently contains:

- [Final report slide deck](./Long%20Nguy%E1%BB%85n%20Ng%E1%BB%8Dc%20Ti%E1%BB%83u%20-%20CS2205.JAN2026.DeCuong.FinalReport.Slide.pptx)
- `README.md`

## Current Status

The repository is currently in the proposal and presentation stage. Source code, experiments, and sample datasets can be added in future updates as the research progresses.

## Author

- Nguyen Ngoc Tieu Long
- University of Information Technology, VNU-HCM
