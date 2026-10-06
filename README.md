# Portuguese Bank Marketing – Term Deposit Prediction

## 📌 Project Overview

This project focuses on predicting whether a customer will subscribe to a term deposit using Machine Learning classification techniques.

The project follows an end-to-end Machine Learning workflow, including data cleaning, data preprocessing, exploratory data analysis, handling class imbalance, feature engineering, model training, model evaluation, hyperparameter tuning, and model comparison.

The main objective is to identify customers who are more likely to subscribe to a term deposit and help the bank's marketing team improve customer targeting and campaign effectiveness.

---

## 🎯 Objectives

* Analyze Portuguese bank marketing campaign data.
* Perform data cleaning and preprocessing.
* Perform exploratory data analysis.
* Identify important features affecting term-deposit subscription.
* Handle class imbalance appropriately.
* Prevent target leakage during model development.
* Train multiple classification algorithms.
* Evaluate models using appropriate performance metrics.
* Compare different Machine Learning models.
* Perform hyperparameter tuning.
* Select a suitable final model based on performance.
* Provide business recommendations to the bank's marketing team.

---

## 🛠️ Technologies & Libraries

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **XGBoost**
* **Imbalanced-learn**
* **Jupyter Notebook**

---

## 🔄 Machine Learning Workflow

```text
Data Collection
      ↓
Data Loading
      ↓
Data Cleaning
      ↓
Data Quality Checks
      ↓
Exploratory Data Analysis
      ↓
Data Preprocessing
      ↓
Target Leakage Removal
      ↓
Train-Test Split
      ↓
Class Imbalance Handling
      ↓
Feature Scaling
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Model Comparison
      ↓
Hyperparameter Tuning
      ↓
Threshold Optimization
      ↓
Final Model Selection
      ↓
Business Recommendations
```

---

## 🤖 Machine Learning Models

The following classification algorithms are implemented and compared:

1. Logistic Regression
2. Support Vector Machine (SVM)
3. Decision Tree Classifier
4. Random Forest Classifier
5. Gradient Boosting Classifier
6. XGBoost Classifier

---

## ⚙️ Data Preprocessing

The following preprocessing steps are performed:

* Dataset inspection
* Missing-value analysis
* Duplicate-value checking
* Data type verification
* Exploratory data analysis
* Encoding of categorical variables
* One-Hot Encoding
* Removal of unnecessary features
* Removal of target leakage
* Train-test splitting
* Feature scaling
* Class imbalance handling

The dataset is split using **stratification** to maintain the target-class distribution between the training and testing datasets.

---

## ⚠️ Target Leakage Handling

The `duration` feature was removed from the dataset before model training.

The duration represents the length of the current marketing call and is only known after the call has taken place.

Using this feature for prediction could result in **target leakage**, because the information would not be available when deciding which customers to contact.

Therefore, `duration` was excluded to create a more realistic predictive model.

---

## ⚖️ Class Imbalance Handling

The target variable contains imbalanced classes, with considerably fewer customers subscribing to term deposits compared with customers who do not subscribe.

**Random Under-Sampling** is applied to the **training data only** to reduce class imbalance.

The test dataset is kept unchanged so that final model performance can be evaluated using the original class distribution.

This helps prevent information leakage from the test set.

---

## 📊 Model Evaluation

The models are evaluated using multiple classification metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix

Because the target classes are imbalanced, **Precision, Recall, F1-Score, and ROC-AUC** are considered important metrics in addition to accuracy.

### Why These Metrics?

**Precision:** Measures how many customers predicted as likely to subscribe actually subscribed.

**Recall:** Measures how many actual subscribers were correctly identified by the model.

**F1-Score:** Provides a balance between Precision and Recall.

**ROC-AUC:** Measures the model's ability to distinguish between customers who subscribe and customers who do not across different classification thresholds.

---

## 📈 Model Comparison

The following Machine Learning models were trained and compared:

| Model                  |
| ---------------------- |
| Logistic Regression    |
| Support Vector Machine |
| Decision Tree          |
| Random Forest          |
| Gradient Boosting      |
| XGBoost                |

The models were compared using **Accuracy, Precision, Recall, F1-Score, and ROC-AUC**.

ROC-AUC was given particular importance because the target variable is imbalanced and accuracy alone may not provide a complete picture of model performance.

---

## 🔧 Hyperparameter Tuning

Hyperparameter tuning was performed to improve the performance of the selected Machine Learning model.

The Random Forest model was tuned using different combinations of parameters such as:

* Number of estimators
* Maximum tree depth
* Minimum samples split
* Minimum samples leaf

The tuned model was then evaluated on the original test dataset.

---

## 🏆 Final Model

The **Tuned Random Forest Classifier** was selected as the final model.

A classification threshold of **0.60** was selected to obtain a better balance between precision and recall for the positive class.

### Final Test Performance

| Metric    |      Score |
| --------- | ---------: |
| Accuracy  |   **0.87** |
| Precision |   **0.45** |
| Recall    |   **0.62** |
| F1-Score  |   **0.52** |
| ROC-AUC   | **0.8112** |

The final model achieved a **ROC-AUC of 0.8112**, indicating good ability to distinguish between customers who are likely and unlikely to subscribe to a term deposit.

---

## 🔍 Feature Importance

The most important features identified by the final Random Forest model include:

* `euribor3m`
* `emp.var.rate`
* `nr.employed`
* `cons.conf.idx`
* `age`
* `pdays`
* `cons.price.idx`
* `poutcome_success`
* `contact_telephone`
* `campaign`

These features can provide useful information for understanding customer behavior and campaign outcomes.

---

## 💼 Business Recommendations

The model can help the bank's marketing team prioritize customers who are more likely to subscribe to a term deposit.

Potential benefits include:

* Improving customer targeting.
* Prioritizing high-potential customers.
* Reducing unnecessary marketing calls.
* Improving marketing campaign efficiency.
* Better allocation of marketing resources.
* Supporting data-driven customer engagement.

The bank can use the model's predicted probabilities to rank customers and focus marketing efforts on higher-probability customers.

---

## ⚠️ Project Limitations

* The dataset contains an imbalanced target variable.
* Some categorical variables contain `unknown` values.
* The model's precision for the positive class is lower than its recall.
* Model performance may change when applied to new customer populations.
* Additional feature engineering and model tuning may further improve performance.

---

## 🚀 Future Improvements

* Experiment with **SMOTE** and other class-imbalance techniques.
* Perform additional **hyperparameter tuning**.
* Use **cross-validation** for more reliable model evaluation.
* Perform advanced feature selection.
* Apply **SHAP** or other model explainability techniques.
* Deploy the model as a **web application or API**.
* Monitor model performance using new customer data.
* Continuously retrain the model with updated marketing campaign data.

---

## 🧰 Tools & Technologies

**Programming:** Python

**Data Analysis:** Pandas, NumPy

**Data Visualization:** Matplotlib, Seaborn

**Machine Learning:** Scikit-learn, XGBoost

**Imbalanced Data:** Imbalanced-learn

**Development Environment:** Jupyter Notebook

---

## 📌 Conclusion

This project demonstrates an end-to-end Machine Learning workflow for predicting customer subscription to a term deposit.

Multiple classification algorithms, including **Logistic Regression, SVM, Decision Tree, Random Forest, Gradient Boosting, and XGBoost**, were trained and compared using multiple evaluation metrics.

After model tuning and threshold optimization, the **Tuned Random Forest Classifier** was selected as the final model.

The final model achieved an **Accuracy of 0.87, Precision of 0.45, Recall of 0.62, F1-Score of 0.52, and ROC-AUC of 0.8112**.

The project demonstrates practical skills in **data preprocessing, exploratory data analysis, categorical encoding, target leakage prevention, class imbalance handling, machine learning, model evaluation, hyperparameter tuning, and business-oriented model interpretation**.
