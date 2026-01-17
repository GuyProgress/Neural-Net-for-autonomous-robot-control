Neural Network–Based Autonomous Robot Control

This repository contains an academic project developed at Arts et Métiers ParisTech (ENSAM – Metz) focused on the design, training, and evaluation of a modular neural-network control system for an autonomous mobile robot.

Project Overview

The control system is composed of two neural networks connected in cascade:

Model A – Regression

Input: 24 ultrasonic sensor readings

Output: 4 aggregated, interpretable distances (Front, Back, Left, Right)

Purpose: dimensionality reduction and noise smoothing

Performance: R² ≈ 0.95, MAE ≈ 0.08

Model B – Classification

Input: 4 aggregated sensor values

Output: robot control command

Classes:

Move-Forward

Sharp-Right-Turn

Slight-Left-Turn

Slight-Right-Turn

Accuracy on exact data: 98.1%

Integrated System (A → B)

End-to-end accuracy: 84%

Total parameters: 1,883

Designed for lightweight, interpretable embedded deployment

Repository Content

Block_regression + sys globale.ipynb
Training, evaluation, and integration of Model A and the full pipeline.

Block_classification.ipynb
Training and analysis of Model B, including performance metrics.

RapportAnn_ELHOUDAIGUI_ES-Salhy.pdf
Full technical report (methodology, experiments, Pareto analysis, SHAP interpretation).

Key Features

Modular architecture (regression + classification)

Hyperparameter study and Pareto trade-off analysis

Multi-seed experiments for robustness

Interpretability via SHAP values

Error propagation analysis in cascaded systems

Technologies

Python

TensorFlow / Keras

NumPy, Pandas, Scikit-learn

Matplotlib, Seaborn, SHAP

Authors

Othmane EL HOUDAIGUI

Mohamed ES-SALHY

January 2026
