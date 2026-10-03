# SWYNEX-Final-Data-Science-Project

Final project of the SWYNEX Technologies Data Science internship: an end-to-end case study combining Problem Statement, Data Preparation, EDA, Modeling, and Conclusions into one documented project.

## Problem Statement
What factors most influenced survival on the Titanic, and can we build a model to predict it from passenger information? Target: `Survived` (binary classification).

## Workflow
1. **Data Preparation** — cleaned 891 raw passenger records (missing Cabin/Age/Embarked, wrong types) down to 0 missing values.
2. **EDA** — found 5 key insights: class, sex, age, family size, and fare/cabin all relate to survival, with sex being the strongest single predictor.
3. **Modeling** — trained Logistic Regression and Random Forest on 6 features (Pclass, Sex, Age, Fare, FamilySize, HasCabin).
4. **Evaluation** — both models reached ~80% accuracy and 0.84 ROC-AUC, beating the 62% majority-class baseline.
5. **Conclusions** — sex, class, age and family size are the strongest predictors; a simple model performs nearly as well as a complex one.

## Results
| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | 0.799 | 0.754 | 0.710 | 0.731 | 0.842 |
| Random Forest | 0.793 | 0.758 | 0.681 | 0.718 | 0.839 |

## Limitations
- Small dataset (891 rows) — a single split can shift results; cross-validation would be more robust.
- Historical, non-representative data.
- Age/Cabin were partly imputed.
- Class imbalance (~38% survived) means accuracy alone isn't reliable.
- No hyperparameter tuning performed.

## Repository contents
| File | Description |
|------|-------------|
| `final_project.ipynb` | Complete end-to-end notebook: problem statement through conclusions |
| `titanic_raw.csv` | Original raw dataset |
| `cleaned_data.csv` | Cleaned dataset (Task 1 output) |
| `eda_summary.png` | 6-panel EDA chart summarizing all 5 insights |
| `final_roc_curves.png` | ROC curves for both models |
| `README.md` | This file |

## How to run
```bash
git clone https://github.com/challasrinuvas/SWYNEX-Final-Data-Science-Project.git
cd SWYNEX-Final-Data-Science-Project
pip install pandas numpy matplotlib scikit-learn jupyter
jupyter notebook final_project.ipynb
```

## Tools
Python, pandas, NumPy, scikit-learn, Matplotlib, Jupyter Notebook

## Related repos (earlier tasks)
- Task 1: https://github.com/challasrinuvas/SWYNEX-Data-Preparation
- Task 2: https://github.com/challasrinuvas/SWYNEX-Exploratory-Data-Analysis
- Task 3: https://github.com/challasrinuvas/SWYNEX-Modeling-and-Evaluation

#SWYNEX #Internship #DataScience
