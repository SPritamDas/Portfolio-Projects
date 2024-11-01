# Project Title: Robust Loan Approval Prediction Using Machine Learning and Deep Learning

## License
This project is licensed under the Apache License 2.0.

## Project Links
- **Kaggle Notebook**: [Robust Loan Approval Prediction Using ML and DL](https://www.kaggle.com/code/shuvendupritam/robust-loan-approval-prediction-using-ml-and-dl)
- **GitHub Repository**: [Loan Approval Prediction Project](https://github.com/SPritamDas/Portfolio-Projects/blob/main/Loan%20Approval%20Prediction/loan-approval-prediction-using-ml-dl-and-auto-ml%20(1).ipynb)

## Overview
The **Robust Loan Approval Prediction** project aims to develop a predictive model for determining loan approval statuses using advanced machine learning (ML) and deep learning (DL) techniques. This initiative responds to the growing need for efficient and reliable loan assessment processes in the financial sector, focusing on minimizing risk and enhancing operational efficiency.

## Dataset Description
The project utilizes a synthetic dataset generated to mimic real-world loan applicant data. This dataset includes features relevant to loan applications, along with a binary target variable indicating loan approval status. The synthetic nature of the dataset allows for the exploration of feature distributions and the application of various machine learning techniques without compromising actual client data.

## Methodology
The methodology encompasses the following key steps:

1. **Data Exploration**: Conduct thorough exploratory data analysis (EDA) to understand feature distributions, relationships, and potential outliers. This includes univariate, bivariate, and multivariate analyses to identify patterns and insights.

2. **Data Preprocessing**: Address class imbalance in the dataset using SMOTE (Synthetic Minority Over-sampling Technique), ensuring robust learning from minority class samples.

3. **Model Development**:
   - **Basic Models**: Implement foundational models such as Logistic Regression, K-Nearest Neighbors, and Decision Trees to establish baseline performance.
   - **Ensemble Techniques**: Employ advanced ensemble methods, including Bagging (Random Forest) and Boosting (XGBoost, AdaBoost, Gradient Boosting, and CatBoost), to enhance predictive accuracy.
   - **Stacking and Voting**: Create stacking and voting classifiers that integrate predictions from multiple models to improve robustness and generalizability.
   - **Deep Learning Models**: Develop artificial neural networks (ANN) using Keras, exploring hyperparameter tuning and advanced techniques to optimize model performance.

4. **Evaluation**: Assess model performance using the area under the ROC curve (AUC), providing insights into the models' ability to differentiate between approved and non-approved loans.

5. **Submission Preparation**: Format the final predictions for submission, ensuring compliance with competition guidelines.

## Model Comparison

| Model                | AUC Score | Description                                     | Hyperparameters                           |
|----------------------|-----------|-------------------------------------------------|-------------------------------------------|
| Logistic Regression   | 0.75      | A statistical model that estimates the probability of a binary outcome. | C=1.0, Solver='lbfgs', Max_iter=100    |
| K-Nearest Neighbors   | 0.78      | A non-parametric method used for classification and regression. | n_neighbors=5, Weights='uniform'        |
| Decision Tree         | 0.76      | A tree-structured model used for classification tasks. | Max_depth=5, Min_samples_split=10      |
| Random Forest         | 0.82      | An ensemble method that constructs multiple decision trees. | N_estimators=100, Max_depth=None       |
| XGBoost              | 0.85      | A boosting method that optimizes the performance through gradient descent. | Learning_rate=0.1, Max_depth=5, N_estimators=100 |
| AdaBoost             | 0.80      | A boosting technique that adjusts weights to improve weak learners. | N_estimators=50, Learning_rate=1.0     |
| Gradient Boosting    | 0.83      | An iterative method that minimizes the loss function. | N_estimators=100, Learning_rate=0.1    |
| CatBoost             | 0.84      | A gradient boosting library that handles categorical features automatically. | Iterations=1000, Learning_rate=0.1      |
| ANN (Keras)          | 0.87      | A deep learning model that simulates a neural network. | Epochs=100, Batch_size=32, Units=64     |
| Meta ANN | | | |
| Weighted Output | | | |


## Conclusion
This project demonstrates the integration of traditional and cutting-edge techniques in loan approval prediction, aiming to deliver a robust and efficient solution for financial institutions. By leveraging a combination of machine learning and deep learning methodologies, we enhance the ability to make data-driven decisions in the lending process, ultimately improving risk management and customer satisfaction.

