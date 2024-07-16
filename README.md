# Loan-Default-Prediction-Model

Rational
Consumer finance providers face significant challenges in accurately predicting loan default risk, especially for clients with little or no credit history. Traditional methods often fail to address the dynamic nature of client behavior, leading to unstable and frequently updated scorecards. A stable and reliable model is essential for making informed lending decisions that balance risk and accessibility.

Introduction
This notebook aims to develop a predictive model to determine which clients are more likely to default on their loans. The goal is to provide a stable and reliable solution that remains effective over time, thus aiding consumer finance providers in making better lending decisions. This project is part of a competition hosted by Home Credit, an international consumer finance provider known for responsible lending practices and financial inclusion efforts.

The competition runs from February 5, 2024, to May 28, 2024, and focuses on using data science to improve the prediction of loan default risk.

A key evaluation criterion is the gini stability metric, which measures the model's predictive performance and stability over time.

Objective
The primary objective of this project is to build a predictive model that accurately assesses the likelihood of loan default while maintaining stability over time. The model should:

Utilize a robust data preprocessing and feature engineering pipeline.
Employ advanced machine learning techniques to maximize predictive accuracy.
Ensure stability in predictions across different time periods to minimize the need for frequent model updates.
Deliverables
Data Preprocessing and Feature Engineering:
1. Read and concatenate multiple datasets.

* Set appropriate data types for columns.
* Handle date features and filter out irrelevant or low-quality columns.
* Engineer additional features to enrich the dataset.
2. Model Training and Evaluation:

* Implement a cross-validation strategy using StratifiedGroupKFold to ensure stable performance evaluation.
* Train a LightGBM classifier and utilize early stopping and logging callbacks.
* Aggregate predictions from multiple cross-validation folds using a custom VotingModel.
3. Prediction and Submission:

* Prepare the test dataset by setting the correct data types and indices.
* Use the trained model to predict probabilities for the test set.
* Create a submission file with case_id and predicted scores.
4. Model Stability Assessment:

* Evaluate the model using the gini stability metric.
* Ensure the model's predictions are stable over different weeks to avoid performance drop-offs.
By achieving these deliverables, the notebook will contribute to developing a reliable and stable predictive model that can help consumer finance providers make better lending decisions and potentially improve financial inclusion for individuals with limited credit history.
