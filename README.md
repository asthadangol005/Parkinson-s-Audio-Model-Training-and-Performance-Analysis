# Parkinson's Disease – Audio-Based Model Training & Evaluation

This repository focuses on building and evaluating machine learning models that detect early signs of Parkinson’s disease using **raw voice recordings**. The goal is to support non-invasive early screening through voice analysis.

## Overview

Early changes in voice can be one of the first indicators of Parkinson’s. This project processes audio recordings, extracts acoustic features, trains ML models, and evaluates their performance for early Parkinson’s risk screening.

## Key Steps in the Pipeline

| Stage | Description |
|-------|--------------|
|Data Acquisition | Raw voice recordings of sustained vowel sounds |
|Preprocessing | Noise removal, silence trimming, normalization |
|Feature Extraction | MFCCs,RMS, zero-crossing rate, spectral contrast, Spectral centroid,F0 |
|Model Training | SVM (RBF), Random Forest, Logistic Regression, TabPFN, SAINT-Lite, TabNet |
|Evaluation | Accuracy, F1-Score, ROC-AUC, Precision-Recall, Confusion Matrix |
| Best Performing Model | **SVM with RBF kernel** (best generalization on test data) |

## Performance Summary

| Model | Train Accuracy | Test Accuracy | F1-Score | AUC |
|--------|---------------|----------------|-------------|--------|
| SVM (RBF) | 91.1% | 84.0% | 83.3% | 87.8% |
| Logistic Regression | 83.9% | 84.0% | 83.3% | 94.9% |
| Random Forest | 85.7% | 80.0% | 79.9% | 90.4% |
| SAINT-Lite | 83.9% | 80.0% | 79.9% | 80.1% |
| TabPFN | 100% (overfit) | 80.0% | 79.5% | 92.3% |
| TabNet | 64.3% | 64.0% | 59.9% | 73.1% |
| Hypertab | 50% | 48.0% | 32.4% | 30.8% |

**SVM (RBF)** was chosen for deployment due to its stable, non-overfitting performance.



