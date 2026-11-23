# Customer Churn Prediction — Machine Learning Research
**Research in progress • FIU CNT 4153**

This page describes the research plan. The assignment notebook, code, data and results are not published here.

## 1. Overview
An FIU CNT 4153 research project asking whether telecommunications account, billing, and service data can predict customer churn. This is supervised classification, not an LLM application or an agent-orchestration project.

## 2. My Role
I am responsible for completing the research, implementing and checking the notebook, evaluating models, and explaining the findings. The inspected artifact is a planning outline; implementation and experimental results are not yet available in that file.

## 3. Planned Technical Stack
Python, Jupyter, pandas, NumPy, matplotlib/seaborn, and scikit-learn. These libraries appear in the research plan; installed versions and executed usage have not been verified.

## 4. Planned Architecture
A notebook workflow will load the approved dataset, inspect and clean it, separate training and test records, fit preprocessing/model pipelines, evaluate held-out predictions, and produce figures and interpretation.

## 5. Planned Functionality
The outline proposes IBM Telco Customer Churn data, exploratory analysis, numeric/categorical preprocessing, Logistic Regression, Random Forest, and comparison with a majority-class baseline.

## 6. Design Decisions
The plan uses the same stratified split for both models, fits learned preprocessing only on training data, excludes customer identifiers as predictors, and distinguishes predictive association from causation. These are planned methods, not completed experiments.

## 7. Testing and Validation
The available notebook is a planning outline with no executed experiments. Dataset shape, missingness, model fit, leakage checks, and metrics remain unverified. Reproducibility requires a clean top-to-bottom execution once the actual notebook is complete.

## 8. Execution Approach
Local or course-approved Jupyter environment. No production model deployment, hosted prediction API, or live customer system is claimed.

## 9. Verified Outcomes
A structured research outline exists. No fitted models, performance rankings, accuracy/precision/recall/F1/ROC-AUC values, or business outcomes have been established.

## 10. Future Considerations
Complete the assignment, verify dataset eligibility and usage terms, record the environment and source/checksum, run the notebook, align presentation figures with results, and request publication approval.
