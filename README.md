# ADCC-Bench

**ADCC-Bench** is a reproducible benchmark framework for anomaly detection in cryptocurrency transactions. It standardizes **modality-aware data splitting** (to avoid temporal leakage), preprocessing, multi-seed evaluation, and statistical testing for fair cross-study comparison.

## Scope
We benchmark **tree-based ensembles** and **graph neural networks (GNNs)** under a unified protocol across heterogeneous blockchain anomaly modalities (transaction-flow, execution-level, behavioral/account-level).

## Datasets
This repository supports experiments on the following datasets (please follow each source’s license/terms):

- **BLTE (labeled Ethereum transactions dataset)** — Springer chapter:  
  `https://link.springer.com/chapter/10.1007%2F978-981-33-6835-4_5`
- **Elliptic++ (transaction-flow / illicit detection)** — ACM KDD paper:  
  `https://dl.acm.org/doi/abs/10.1145/3580305.3599803`
- **Ethereum Fraud Detection (account-level features)** — Kaggle dataset:  
  `https://www.kaggle.com/datasets/vagifa/ethereum-frauddetection-dataset/data`

## Benchmark protocol (high level)
- **Splitting**: chronological split for dynamic transaction graphs; stratified splits for static/aggregated profiles.
- **Training**: unified tuning (validation-based) and final retraining on train+val.
- **Evaluation**: Macro-F1 / AUC-ROC with **multi-seed runs** and **Welch’s t-test** for stability and significance.
- **Explainability**: SHAP-based attribution for feature-centric models.

## Models
- Tree-based: Random Forest, XGBoost, LightGBM  
- Graph-based: GCN, GraphSAGE  
- Optional: hard/soft voting ensembles (when applicable)

## Reproducibility
- Fixed random seeds (multi-run) and standardized preprocessing.
- Report results as **mean ± std** over multiple seeds.

