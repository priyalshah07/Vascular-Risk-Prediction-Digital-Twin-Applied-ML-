# Vascular-Risk-Prediction-Digital-Twin-Applied-ML-
An explainable ML system that predicts vascular risk and simulates how real-world improvements can change patient outcomes.

## Project Overview

This project builds an end-to-end applied machine learning system to predict early vascular disease risk and translate predictions into actionable insights. Beyond classification, the project emphasizes explainability, robustness, and decision support, demonstrating how ML models can be responsibly used in health-related contexts.

The system combines interpretable modeling, model explainability, and patient-level “what-if” simulations to move from risk prediction to risk understanding and intervention planning.

## Key Features

* Interpretable Baseline Model
Trained a logistic regression model to predict vascular disease risk, achieving ROC-AUC ≈ 0.97 with high recall for high-risk patients. Model choice prioritizes interpretability and reliability.

* Explainable AI (Global + Local)
Used model coefficients and SHAP to analyze:
- Population-level drivers of risk
- Patient-level explanations for individual predictions
This ensures predictions are driven by meaningful physiological patterns rather than proxy variables.

* Digital Twin & Scenario Simulation
Implemented a patient-level digital twin to simulate realistic “what-if” scenarios (e.g., improved blood pressure, increased exercise capacity).
Demonstrated that combined improvements reduced predicted risk by ~40%, turning the model into a decision-support tool rather than a static classifier.

* Model Robustness Check
Trained a Gradient Boosting model as a higher-capacity alternative. While accuracy improved slightly, logistic regression achieved better ROC-AUC and interpretability, and was retained as the final model—highlighting principled model selection.

## Why This Project Matters

Most ML projects stop at prediction. This project goes further by:

- Explaining why predictions are made

- Demonstrating how risk can change under realistic interventions

- Balancing performance with interpretability and usability

The result is a practical, explainable, and decision-oriented ML system, aligned with real-world applied AI workflows.

## Tech Stack

- Languages & Libraries: Python, pandas, NumPy, scikit-learn

- Modeling: Logistic Regression, Gradient Boosting

- Explainability: SHAP

- Visualization: Matplotlib

- Techniques: Feature Engineering, Model Evaluation, Explainable AI, Scenario Simulation

## Data used

This project uses the Cleveland Heart Disease dataset, a widely referenced benchmark dataset for cardiovascular risk modeling. The dataset contains structured patient-level features capturing demographics, exercise response, stress indicators, and disease burden, making it well suited for applied risk prediction and explainability-focused modeling.

Source: UCI Machine Learning Repository \
Original Provider: Cleveland Clinic Foundation \
Records: 303 patients \
Features: 13 input features + 1 target label \
Target: Presence or absence of clinically significant vascular disease

The dataset was sourced from:
https://archive.ics.uci.edu/ml/datasets/heart+Disease

## Project Structure
``` text
predictvasc/
├── data/                     # Dataset (Cleveland subset)
├── notebooks/                # Data prep, modeling, explainability
├── src/                      # Reusable preprocessing / utilities
├── README.md
└── requirements.txt
```

## Key Takeaway

This project demonstrates how interpretable machine learning, explainability, and scenario simulation can be combined to build AI systems that are not only accurate, but also trustworthy and actionable.
