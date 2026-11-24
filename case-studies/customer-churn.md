# Customer Churn Prediction — Machine Learning Research
**Miangelisse Encarnacion • FIU CNT 4153**

A technical summary of my academic research. The assignment notebook, source code, dataset, and submission files are not included in this repository.

## 1. Overview and Research Question
I investigated whether telecommunications account, billing, and service information could predict customer churn. I compared Logistic Regression and Random Forest to determine how well they identified customers who left, rather than relying on overall accuracy alone.

## 2. My Role
I implemented the analysis in Python: inspecting the dataset, cleaning records, engineering features, preparing training and test sets, fitting both models, evaluating their predictions, and interpreting the findings.

## 3. Technical Stack
Python, Jupyter, pandas, NumPy, matplotlib, seaborn, and scikit-learn.

## 4. Analysis Workflow
The workflow covered dataset inspection, exploratory analysis, cleaning, feature engineering, a stratified train/test split, model-specific pipelines, held-out evaluation, and interpretation.

Both models used the same training and test records. Learned preprocessing was fitted on the training data through scikit-learn pipelines.

## 5. Data Preparation and Feature Engineering
The notebook's recorded outputs show 7,043 records and 21 original columns in the IBM Telco Customer Churn dataset.

I converted total charges from text to numeric values, excluded 11 records missing that value, checked for duplicate customer identifiers, removed the identifier from predictive features, and encoded the churn target. The cleaned data contained 7,032 records.

I added tenure groups and a count of seven selected subscribed services. These features summarize existing customer information; they do not use the churn outcome.

Exploratory analysis examined class imbalance and observed churn rates across contract types. These are descriptive associations, not evidence of causation.

## 6. Model Design Decisions
I used a stratified 80/20 split with a fixed random seed, producing 5,625 training records and 1,407 test records.

Numeric preprocessing included median imputation and standardization. Categorical preprocessing included most-frequent imputation and one-hot encoding configured to handle unseen categories. I compared Logistic Regression with a 150-tree Random Forest.

An always-predict-no baseline established why accuracy alone is insufficient: predicting that every customer stays can look reasonably accurate while missing every customer who churns.

## 7. Evaluation and Recorded Results
I evaluated accuracy, precision, recall, F1-score, and ROC-AUC, alongside confusion matrices, ROC curves, and a metric comparison chart.

The following values are rounded results saved in my notebook. They were reviewed for this summary but have not been independently reproduced in a fresh environment.

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
| --- | ---: | ---: | ---: | ---: | ---: |
| Always predict no | 0.734 | 0.000 | 0.000 | 0.000 | 0.500 |
| Logistic Regression | **0.794** | **0.635** | **0.529** | **0.577** | **0.835** |
| Random Forest | 0.781 | 0.611 | 0.484 | 0.540 | 0.815 |

## 8. Findings and Interpretation
Logistic Regression performed better across the reported measures on this split. Its 52.9% recall means it identified just over half of the actual churners, so its higher accuracy does not make it a complete retention solution.

The fitted Random Forest assigned the highest feature importances to total charges, monthly charges, and tenure. These rankings describe that forest's use of features; they do not establish the causes of churn or explain Logistic Regression's predictions.

## 9. Execution and Limitations
This is notebook-based academic research, with no deployed prediction API or production customer system.

Results come from one dataset and one train/test split. Cross-validation, hyperparameter tuning, threshold selection, independent-data evaluation, and a clean-environment reproduction remain future work. The study does not establish causal effects or measured improvements in customer retention.

## 10. Future Development
Further work could evaluate class-imbalance strategies, tune models using training-only validation, compare decision thresholds, and test on independent data. A reproducible public code release would require a separately reviewed environment and dataset instructions after academic sharing approval.

Only this explanation and aggregate findings are public. The academic implementation and submission materials remain unpublished.
