# Hyperparameter search ranges aggregated from executed notebooks

## Scope and method
- Parsed code and printed outputs in notebooks under each dataset folder.
- Only ranges/distributions actually defined in the random search blocks are included.
- All tree-model searches use `n_iter=30` (30 sampled configurations/model).

## BLTE dataset (`blte/`)
| Model | Hyperparameter | Search range/distribution |
|---|---|---|
| RandomForest | n_estimators | randint(200, 600) |
| RandomForest | max_depth | randint(3, 30) |
| RandomForest | min_samples_split | randint(2, 50) |
| RandomForest | min_samples_leaf | randint(1, 20) |
| RandomForest | max_features | ["sqrt", "log2", None] |
| RandomForest | class_weight | [None, "balanced"] |
| RandomForest | criterion | ["gini", "entropy"] |
| XGBoost | n_estimators | randint(300, 800) |
| XGBoost | max_depth | randint(3, 10) |
| XGBoost | learning_rate | uniform(0.01, 0.2) |
| XGBoost | subsample | uniform(0.6, 0.4) |
| XGBoost | colsample_bytree | uniform(0.6, 0.4) |
| XGBoost | min_child_weight | randint(1, 10) |
| XGBoost | gamma | uniform(0, 5) |
| XGBoost | reg_lambda | uniform(0, 5) |
| XGBoost | objective | ["binary:logistic"] |
| XGBoost | eval_metric | ["logloss", "aucpr"] |
| LightGBM | n_estimators | randint(300, 800) |
| LightGBM | num_leaves | randint(15, 255) |
| LightGBM | max_depth | randint(-1, 12) |
| LightGBM | learning_rate | uniform(0.01, 0.2) |
| LightGBM | subsample | uniform(0.6, 0.4) |
| LightGBM | colsample_bytree | uniform(0.6, 0.4) |
| LightGBM | min_child_samples | randint(10, 100) |
| LightGBM | reg_lambda | uniform(0, 5) |
| LightGBM | objective | ["binary"] |
| LightGBM | metric | ["binary_logloss", "auc", "aucpr"] |

## Ethereum Fraud Detection dataset (`Ethereum Fraud Detection Dataset/`)
| Model | Hyperparameter | Search range/distribution |
|---|---|---|
| RandomForest | n_estimators | randint(200, 600) |
| RandomForest | max_depth | randint(3, 30) |
| RandomForest | min_samples_split | randint(2, 50) |
| RandomForest | min_samples_leaf | randint(1, 20) |
| RandomForest | max_features | ["sqrt", "log2", None] |
| RandomForest | class_weight | [None, "balanced"] |
| RandomForest | criterion | ["gini", "entropy"] |
| XGBoost | n_estimators | randint(300, 800) |
| XGBoost | max_depth | randint(3, 10) |
| XGBoost | learning_rate | uniform(0.01, 0.2) |
| XGBoost | subsample | uniform(0.6, 0.4) |
| XGBoost | colsample_bytree | uniform(0.6, 0.4) |
| XGBoost | min_child_weight | randint(1, 10) |
| XGBoost | gamma | uniform(0, 5) |
| XGBoost | reg_lambda | uniform(0, 5) |
| XGBoost | objective | ["binary:logistic"] |
| XGBoost | eval_metric | ["logloss", "aucpr"] |
| LightGBM | n_estimators | randint(300, 800) |
| LightGBM | max_depth | randint(3, 10) |
| LightGBM | learning_rate | uniform(0.01, 0.2) |
| LightGBM | subsample | uniform(0.6, 0.4) |
| LightGBM | colsample_bytree | uniform(0.6, 0.4) |
| LightGBM | min_child_weight | randint(1, 10) |
| LightGBM | gamma | uniform(0, 5) |
| LightGBM | reg_lambda | uniform(0, 5) |
| LightGBM | objective | ["binary"] |
| LightGBM | eval_metric | ["logloss", "aucpr"] |

## Elliptic++ dataset (`elliptic/`)

### Notebook: `tree_random_70_15_15.ipynb`
| Model | Hyperparameter | Search range/distribution |
|---|---|---|
| RandomForest | n_estimators | randint(200, 600) |
| RandomForest | max_depth | randint(3, 30) |
| RandomForest | min_samples_split | randint(2, 50) |
| RandomForest | min_samples_leaf | randint(1, 20) |
| RandomForest | max_features | ["sqrt", "log2", None] |
| RandomForest | class_weight | [None, "balanced"] |
| RandomForest | criterion | ["gini", "entropy"] |
| XGBoost | n_estimators | randint(200, 800) |
| XGBoost | max_depth | randint(3, 12) |
| XGBoost | learning_rate | uniform(0.01, 0.29) |
| XGBoost | subsample | uniform(0.6, 0.4) |
| XGBoost | colsample_bytree | uniform(0.6, 0.4) |
| XGBoost | min_child_weight | randint(1, 10) |
| XGBoost | reg_lambda | uniform(0, 5) |
| XGBoost | objective | ["binary:logistic"] |
| XGBoost | eval_metric | ["logloss", "aucpr"] |
| XGBoost | scale_pos_weight | [scale_pos_weight] |
| LightGBM | n_estimators | randint(200, 800) |
| LightGBM | num_leaves | randint(15, 255) |
| LightGBM | max_depth | randint(3, 12) |
| LightGBM | learning_rate | uniform(0.01, 0.29) |
| LightGBM | subsample | uniform(0.6, 0.4) |
| LightGBM | colsample_bytree | uniform(0.6, 0.4) |
| LightGBM | min_child_samples | randint(10, 100) |
| LightGBM | reg_lambda | uniform(0, 5) |
| LightGBM | objective | ["binary"] |
| LightGBM | metric | ["binary_logloss", "auc", "aucpr"] |
| LightGBM | scale_pos_weight | [scale_pos_weight] |

### Notebook: `tree_with_gnn_ensemble.ipynb`
| Model | Hyperparameter | Search range/distribution |
|---|---|---|
| RandomForest | n_estimators | randint(200, 600) |
| RandomForest | max_depth | randint(3, 30) |
| RandomForest | min_samples_split | randint(2, 50) |
| RandomForest | min_samples_leaf | randint(1, 20) |
| RandomForest | max_features | ["sqrt", "log2", None] |
| RandomForest | class_weight | [None, "balanced"] |
| RandomForest | criterion | ["gini", "entropy"] |
| XGBoost | n_estimators | randint(200, 800) |
| XGBoost | max_depth | randint(3, 12) |
| XGBoost | learning_rate | uniform(0.01, 0.29) |
| XGBoost | subsample | uniform(0.6, 0.4) |
| XGBoost | colsample_bytree | uniform(0.6, 0.4) |
| XGBoost | min_child_weight | randint(1, 10) |
| XGBoost | reg_lambda | uniform(0, 5) |
| XGBoost | objective | ["binary:logistic"] |
| XGBoost | eval_metric | ["logloss", "aucpr"] |
| XGBoost | scale_pos_weight | [scale_pos_weight] |
| LightGBM | n_estimators | randint(200, 800) |
| LightGBM | num_leaves | randint(15, 255) |
| LightGBM | max_depth | randint(3, 12) |
| LightGBM | learning_rate | uniform(0.01, 0.29) |
| LightGBM | subsample | uniform(0.6, 0.4) |
| LightGBM | colsample_bytree | uniform(0.6, 0.4) |
| LightGBM | min_child_samples | randint(10, 100) |
| LightGBM | reg_lambda | uniform(0, 5) |
| LightGBM | objective | ["binary"] |
| LightGBM | metric | ["binary_logloss", "auc", "aucpr"] |
| LightGBM | scale_pos_weight | [scale_pos_weight] |

### Notebooks without grid/random search blocks
- `elliptic/txs-gcn.ipynb`
- `elliptic/txs_sage.ipynb`
- `blte/blte_gcn.ipynb`
- `blte/blte_sage.ipynb`

These notebooks do not define tree-model `param_dist` dictionaries or `GridSearchCV`/`RandomizedSearchCV` tuning blocks.
