# Early Warning System (EWS) for Risk Detection

## Overview
This project implements an **Early Warning System (EWS)** to identify emerging risks and anomalies in financial and operational data before they escalate into critical issues. The system leverages a combination of **supervised, unsupervised, deep learning, and ensemble methods** to enhance predictive accuracy and robustness.

By continuously monitoring key indicators and analyzing data in real time, the EWS provides actionable alerts that help decision-makers take timely action, minimizing potential losses and safeguarding assets.

## Methodology
The project focuses on **robust anomaly detection** using diverse machine learning techniques:

- **Supervised Learning**: Models trained on labeled data to detect risky or anomalous events.  
- **Unsupervised Learning**: Models that identify outliers and unusual patterns without prior labels.  
- **Deep Learning**: Neural networks, including Variational Autoencoders (VAE), for complex pattern recognition.  
- **Ensemble Methods**: Combines predictions from multiple models (e.g., XGBoost, SVM, Isolation Forest, VAE) to create stronger overall predictors.  

### Ensemble Strategy
1. Evaluate all possible combinations of 2, 3, and 4 models from a predefined set.  
2. Train a **logistic regression meta-model** on the stacked predictions for each combination.  
3. Compute key performance metrics: Precision, Recall, F1-score, ROC AUC.  
4. Calculate **average error correlation** among selected models to promote diversity.  
5. Select the best-performing ensemble for each combination size based on lowest error correlation.  
6. Visualize performance using confusion matrices and other summary plots.

This approach leverages the complementary strengths of heterogeneous models to improve **robustness and predictive accuracy**, especially for detecting critical financial anomalies.
