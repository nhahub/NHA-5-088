# Machine Learning

Predicts whether a scheduled flight will arrive 15 or more minutes late (Q7).

**Owner:** Omar Emad Hamdy (ML Engineer)

---

## What goes here

* Feature table built from the Gold layer, using only information known before departure
* Training and evaluation: logistic regression baseline, then LightGBM; ROC-AUC and PR-AUC
* MLflow experiment tracking
* FastAPI prediction endpoint and its documentation

## Validation

Time-based split: train July–October, validate November, test December 2025.

## Azure equivalent

Azure Machine Learning.
