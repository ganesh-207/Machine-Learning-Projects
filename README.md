🏭 **Machine Failure Prediction — Predictive Maintenance using Machine Learning**

📌**Project Overview**
This project focuses on predicting machine failure in a manufacturing environment using sensor readings and operational data. The goal is to support predictive maintenance, reduce downtime, and optimize plant efficiency by identifying failures before they occur.

🚀 **Key Highlights**
Built a complete end-to-end Machine Learning pipeline Engineered features from temperature, torque, tool wear, and speed
Handled imbalanced data using SMOTE Selected the best model through systematic evaluation
Delivered high recall for failure class
Exported predictions for new unseen data

📂 **Dataset Summary**
The dataset contains machine operational parameters and failure type indicators.

**Features Include:**
Air Temperature (K)
Process Temperature (K)
Rotational Speed (rpm)
Torque (Nm)
Tool Wear (min)
Failure Flags (TWF, HDF, PWF, OSF, RNF)
Target Variable: Machine Failure

**Data was clean, consistent, and contained no missing values.**

**🔧 Workflow Summary**
1️⃣**Data Preprocessing**

Cleaned and standardized features
Encoded product "Type"
Removed unnecessary characters from "Product ID"
Split data into train-test sets

2️⃣ **Handling Class Imbalance**

Machine failures were rare → dataset was highly imbalanced.
SMOTE applied on train data set ensure fair comparison.

3️⃣ **Model Selection**

**Algorithms evaluated:**
Logistic Regression
Decision Tree
Random Forest
BernoulliNB Naive Bayes
XGBoost

**Evaluation Metrics Used:**
Accuracy
Precision
Recall
F1-score
ROC–AUC

**Confusion Matrix**

➡️ **Random Forest consistently performed best for minority-class detection.**

4️⃣ **Final Model**

Random Forest Classifier
Produced high recall for failure detection

5️⃣ **Predictions & Export**

**Predicted machine failure labels for new input data and exported:**
Predicted Machine Failure Results.csv

📊 **Results Summary**

**Metric score for Class 0 (no failure)**
Precision-1.00
Recall-0.98
F1-score-1.00

**Metric score for Class 1(Failure)**
Precision-0.40
Recall-0.83
F1-score-0.54

**Overall Accuracy:** 0.98
**ROC–AUC (Test Set):** 0.96

**Although accuracy is high due to class imbalance, recall and F1-score were prioritized because missing a machine failure can be costly.
ROC–AUC Score: 0.96 → Demonstrates strong separability between failure and non-failure classes.**

🧠 **Insights from Feature Importance**

**Most influential parameters were:**
Torque (Nm)
Rotational speed (rpm)
OSF (Overstrain Failure indicator)
Tool wear (min)
HDF (Heat Dissipation Failure indicator)
TWF (Thermal Wear Failure indicator)
PWF (Power Failure indicator)
Temp_diff (Temperature difference between process & air)
Air temperature (K)
**These variables strongly contribute to predicting machine failures.**

🏁 **Conclusion**

**The final model is highly effective in predicting machine failures and can support industries in:**
Reducing downtime
Planning preventive maintenance
Lowering operational risk
Improving production efficiency

🔮 **Future Enhancements**

Integrate with real-time sensor streaming
Implement model monitoring for drift
Deploy as an API for live predictions

👤 **Author**

**Ganesh**
Machine Learning & Data Science Enthusiast
