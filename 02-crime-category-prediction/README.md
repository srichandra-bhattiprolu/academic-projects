# CrimeCast: Crime Category Prediction

An end-to-end machine learning project from the IIT Madras Data Science programme (Kaggle competition *CrimeCast: Forecasting Crime Categories*, Jul–Sep 2024). Each crime incident record includes location, time, victim details, weapon and modus operandi, and the model predicts which crime category the incident belongs to.

📓 **Notebook:** [`CrimeCast.ipynb`](CrimeCast.ipynb). All outputs and charts are saved in it, so you can read it on GitHub without running anything. If GitHub's preview doesn't load, [open it in nbviewer](https://nbviewer.org/github/srichandra-bhattiprolu/academic-projects/blob/main/02-crime-category-prediction/CrimeCast.ipynb).

## What I did

1. **EDA:** Studied the feature types, null values (several columns are more than 50% empty) and how crime types are spread across the 21 areas, using plots.
2. **Cleaning & imputation:** Dropped or filled sparse columns and handled missing values.
3. **Preprocessing:** Parsed dates and times, split the multi-code *Modus Operandi* field, one-hot encoded categoricals, and lined up the train and test columns.
4. **Feature engineering:** Compared PCA (feature extraction) with SelectKBest (feature selection).
5. **Modelling:** Trained and tuned 6 models with RandomizedSearchCV.

## Results (validation set)

| Model | Accuracy |
| --- | --- |
| Logistic Regression | 84.8% |
| KNN | 80.7% |
| Decision Tree | 87.7% |
| Bagging Classifier | 92.3% |
| MLP Classifier | 83.4% |
| **Gradient Boosting** (lr=0.01, depth=5, 273 trees) | **92.5%** |

Gradient Boosting was the final model and was used for the competition submission.

## Tech

Python · Pandas · NumPy · scikit-learn · Matplotlib · Seaborn · Kaggle

## Run it yourself

The notebook reads its data from the Kaggle competition (`/kaggle/input/crime-cast-forecasting-crime-categories/`). The easiest way to run it is to open it in a Kaggle notebook with that dataset attached.
