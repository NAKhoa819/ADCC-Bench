# Hyperparameter search ranges aggregated from executed notebooks

## Scope and method
- Parsed code and printed outputs in notebooks under each dataset folder.
- Only ranges/distributions actually defined in the random search blocks are included.
- All tree-model searches use `n_iter=30` (30 sampled configurations/model).

## Grouped view (merge identical tables)

### A) RandomForest (identical across all 3 datasets: BLTE, Ethereum, Elliptic)
| Hyperparameter | Search range/distribution |
|---|---|
| n_estimators | randint(200, 600) |
| max_depth | randint(3, 30) |
| min_samples_split | randint(2, 50) |
| min_samples_leaf | randint(1, 20) |
| max_features | ["sqrt", "log2", None] |
| class_weight | [None, "balanced"] |
| criterion | ["gini", "entropy"] |

### B) XGBoost

#### B1. BLTE + Ethereum (identical)
| Hyperparameter | Search range/distribution |
|---|---|
| n_estimators | randint(300, 800) |
| max_depth | randint(3, 10) |
| learning_rate | uniform(0.01, 0.2) |
| subsample | uniform(0.6, 0.4) |
| colsample_bytree | uniform(0.6, 0.4) |
| min_child_weight | randint(1, 10) |
| gamma | uniform(0, 5) |
| reg_lambda | uniform(0, 5) |
| objective | ["binary:logistic"] |
| eval_metric | ["logloss", "aucpr"] |

#### B2. Elliptic (identical in both tree notebooks)
| Hyperparameter | Search range/distribution |
|---|---|
| n_estimators | randint(200, 800) |
| max_depth | randint(3, 12) |
| learning_rate | uniform(0.01, 0.29) |
| subsample | uniform(0.6, 0.4) |
| colsample_bytree | uniform(0.6, 0.4) |
| min_child_weight | randint(1, 10) |
| reg_lambda | uniform(0, 5) |
| objective | ["binary:logistic"] |
| eval_metric | ["logloss", "aucpr"] |
| scale_pos_weight | [scale_pos_weight] |

### C) LightGBM

#### C1. BLTE
| Hyperparameter | Search range/distribution |
|---|---|
| n_estimators | randint(300, 800) |
| num_leaves | randint(15, 255) |
| max_depth | randint(-1, 12) |
| learning_rate | uniform(0.01, 0.2) |
| subsample | uniform(0.6, 0.4) |
| colsample_bytree | uniform(0.6, 0.4) |
| min_child_samples | randint(10, 100) |
| reg_lambda | uniform(0, 5) |
| objective | ["binary"] |
| metric | ["binary_logloss", "auc", "aucpr"] |

#### C2. Ethereum
| Hyperparameter | Search range/distribution |
|---|---|
| n_estimators | randint(300, 800) |
| max_depth | randint(3, 10) |
| learning_rate | uniform(0.01, 0.2) |
| subsample | uniform(0.6, 0.4) |
| colsample_bytree | uniform(0.6, 0.4) |
| min_child_weight | randint(1, 10) |
| gamma | uniform(0, 5) |
| reg_lambda | uniform(0, 5) |
| objective | ["binary"] |
| eval_metric | ["logloss", "aucpr"] |

#### C3. Elliptic (identical in both tree notebooks)
| Hyperparameter | Search range/distribution |
|---|---|
| n_estimators | randint(200, 800) |
| num_leaves | randint(15, 255) |
| max_depth | randint(3, 12) |
| learning_rate | uniform(0.01, 0.29) |
| subsample | uniform(0.6, 0.4) |
| colsample_bytree | uniform(0.6, 0.4) |
| min_child_samples | randint(10, 100) |
| reg_lambda | uniform(0, 5) |
| objective | ["binary"] |
| metric | ["binary_logloss", "auc", "aucpr"] |
| scale_pos_weight | [scale_pos_weight] |

## Notebook coverage notes
- Elliptic notebooks with tree-model search blocks:
  - `elliptic/tree_random_70_15_15.ipynb`
  - `elliptic/tree_with_gnn_ensemble.ipynb`
- Notebooks without explicit tree-model `param_dist` search blocks:
  - `elliptic/txs-gcn.ipynb`
  - `elliptic/txs_sage.ipynb`
  - `blte/blte_gcn.ipynb`
  - `blte/blte_sage.ipynb`
