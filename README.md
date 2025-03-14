# Lung-Cancer-Detection-Model

## Overview
This project uses a **Random Forest Classifier** to predict lung cancer based on patient data.  
The model achieves **96% accuracy** with an **F1-score of 0.84**.  

🚀 Built using **Python, Scikit-Learn, Pandas, and Matplotlib**.  

## Technology Used

- Python (3.12.7)
- Scikit-Learn
- Pandas
- NumPy
- Matplotlib & Seaborn (for data visualization)
  
## Dataset
- The dataset is sourced from [Kaggle]. It contains patient details and lung cancer labels.
- It includes features like `chest pain `, `smoking history`, `cough`, etc.

## Predictive Variables in This Project
### YELLOW_FINGERS
Description: This variable indicates whether a person has yellow fingers, which may be a sign of smoking or other health conditions.
Relevance: Yellow fingers could suggest a history of smoking, which is often correlated with lung diseases or other respiratory issues.

### ANXIETY
Description: This variable represents whether the individual suffers from anxiety.
Relevance: Anxiety can influence overall health, and its relationship with physical health conditions may be an important factor in predicting certain health outcomes.

### CHRONIC DISEASE
Description: Indicates whether the individual has been diagnosed with any chronic diseases like asthma, diabetes, or hypertension.
Relevance: Chronic diseases often increase vulnerability to other health conditions, making this variable crucial for health-related predictions.

### WHEEZING
Description: Represents whether the individual experiences wheezing, a high-pitched whistling sound when exhaling.
Relevance: Wheezing is a common symptom of respiratory issues such as asthma, COPD, or lung infections. It is a strong indicator of respiratory health.

### ALCOHOL CONSUMING
Description: This variable indicates whether the individual consumes alcohol.
Relevance: Alcohol consumption can have various health impacts, including liver diseases, cardiovascular issues, and weakened immune responses.

### CHEST PAIN
Description: This variable indicates whether the individual experiences chest pain.
Relevance: Chest pain is a critical symptom often linked to heart disease or lung-related issues like pneumonia or lung cancer. It is a major factor in predicting serious health conditions.

### SWALLOWING DIFFICULTY
Description: Indicates whether the individual faces difficulty swallowing.
Relevance: Swallowing difficulty could point to issues like esophageal disorders, nerve damage, or more severe conditions such as throat cancer. It's important for identifying various health risks.

### COUGHING
Description: Represents whether the individual experiences frequent coughing.
Relevance: Persistent coughing is often linked to respiratory conditions, such as chronic bronchitis, asthma, or lung infections. It can be a red flag for several health conditions.

## Exploratory Data Analysis

- Checked for missing values ✅
- Visualized feature distributions ✅
- Correlation analysis between features ✅


## Feature Importance

🔹 What is Feature Importance?
Feature importance is a technique used to determine which input features (variables) have the most influence on the model's predictions. In decision tree-based models like Random Forest, the importance of a feature is measured by how much it reduces impurity (e.g., Gini impurity or entropy) across all decision trees in the ensemble.

🔹 Why is Feature Importance Useful?
Improves Model Interpretability → Helps understand which features contribute most to predictions.
Feature Selection → Allows removing less important features to improve efficiency.
Bias Detection → Helps identify if a model is relying too much on certain variables.
Reduces Overfitting → Eliminates unnecessary variables, improving generalization.
🔹 How Feature Importance is Calculated in Random Forest?
Random Forest computes feature importance using two main techniques:

1️⃣ Mean Decrease in Impurity (MDI)
Measures the average decrease in impurity when splitting on a feature across all trees.
Features that lead to more pure splits (fewer misclassifications) are more important.
2️⃣ Mean Decrease in Accuracy (MDA) (Permutation Importance)
Shuffles feature values and observes the drop in model accuracy.
If accuracy drops significantly, the feature is important.
More robust than MDI but computationally expensive.

### Model's Feature Importance
![Output](https://github.com/user-attachments/assets/6757c94c-696e-4cc1-aaee-ce91cc553a79)

## Confusion Matrix
🔹 What is a Confusion Matrix?
A confusion matrix is a performance measurement tool for classification models. It summarizes the correct and incorrect predictions made by a model.

🔹 Structure of Confusion Matrix
For a binary classification problem, the confusion matrix looks like this:

Actual \ Predicted	Positive (1)	Negative (0)
Positive (1)	True Positives (TP)	False Negatives (FN)
Negative (0)	False Positives (FP)	True Negatives (TN)
True Positives (TP) → Correctly predicted positive cases.
True Negatives (TN) → Correctly predicted negative cases.
False Positives (FP) → Incorrectly predicted positives (Type 1 Error).
False Negatives (FN) → Missed positive cases (Type 2 Error).

🔹 Insights from the Confusion Matrix
High TP & TN → Good model performance
High FP → Model incorrectly classifies negatives as positives (over-sensitive model).
High FN → Model misses positive cases (under-sensitive model).
📊 Example Interpretation (Model's Confusion Matrix: [8 2, 1 67])

### Model's Confusion Matrix
![download](https://github.com/user-attachments/assets/28795cee-d097-4e40-8b45-2aca78eca7b2)


8 True Positives → 8 actual positives were correctly classified.
2 False Negatives → The model missed 2 actual positives.
1 False Positive → The model incorrectly classified 1 negative as positive.
67 True Negatives → 67 negatives were correctly classified.

## Model Training and Evaluation 
- Model Used: **Random Forest Classifier**
- Accuracy: **96%**

- Precision: **89%**
- Recall: **80%**
- F1-Score: **84%**

![Screenshot (55)](https://github.com/user-attachments/assets/1d3e8c56-dfc9-44d7-aece-ca89b69c7ffd)

## ROC ( Receiver Operating Characteristic Curve )
🔹 What is an ROC Curve?
The ROC Curve is a graphical representation of a model’s ability to distinguish between positive and negative classes.

 ![Screenshot (8)](https://github.com/user-attachments/assets/8c331ad8-4e84-4c3b-aaf3-97829c63f6c4)

🔹 How to Interpret the ROC Curve?
AUC (Area Under Curve) = 1 → Perfect classifier (ideal scenario).
AUC > 0.9 → Excellent model.
AUC ~ 0.8 → Good model but could improve.
AUC = 0.5 → Model is no better than random guessing.
📊 Model's Interpretation (Model's ROC Curve)
The Model's AUC = 0.96, That means the model is highly effective at distinguishing between classes.
The steeper the curve towards the top-left, the better the model performs.
If the curve is too close to the diagonal, the model is performing poorly.

### Model's ROC Curve
![download (1)](https://github.com/user-attachments/assets/14030568-64a9-4594-b505-bff8037bb6ba)


## Results & Insights
- **High precision (89%)** ensures fewer false positives.  
- **Recall (80%)** suggests potential improvements in sensitivity.  
- **Random Forest works well, but hyperparameter tuning can improve results.**  



