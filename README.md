🏭 **Machine Failure Prediction — Predictive Maintenance using Machine Learning**

📌**Project Overview**<br>
This project focuses on predicting machine failure in a manufacturing environment using sensor readings and operational data. The goal is to support predictive maintenance, reduce downtime, and optimize plant efficiency by identifying failures before they occur.

🚀 **Key Highlights**<br>
Built a complete end-to-end Machine Learning pipeline Engineered features from temperature, torque, tool wear, and speed
Handled imbalanced data using SMOTE Selected the best model through systematic evaluation
Delivered high recall for failure class
Exported predictions for new unseen data

📂 **Dataset Summary**<br>
The dataset contains machine operational parameters and failure type indicators.

**Features Include:** <br>
Air Temperature (K)<br>
Process Temperature (K)<br>
Rotational Speed (rpm)<br>
Torque (Nm)<br>
Tool Wear (min)<br>
Failure Flags (TWF, HDF, PWF, OSF, RNF)<br>
Target Variable: Machine Failure

**Data was clean, consistent, and contained no missing values.**

**🔧 Workflow Summary**<br>
1️⃣**Data Preprocessing**

Cleaned and standardized features<br>
Encoded product "Type"<br>
Removed unnecessary characters from "Product ID"<br>
Split data into train-test sets<br>

2️⃣ **Handling Class Imbalance**

Machine failures were rare → dataset was highly imbalanced.<br>
SMOTE applied on train data set ensure fair comparison.<br>

3️⃣ **Model Selection**

**Algorithms evaluated:**<br>
Logistic Regression<br>
Decision Tree<br>
Random Forest<br>
BernoulliNB Naive Bayes<br>
XGBoost<br>

**Evaluation Metrics Used:**<br>
Accuracy<br>
Precision<br>
Recall<br>
F1-score<br>
ROC–AUC<br>

**Confusion Matrix**

➡️ **Random Forest consistently performed best for minority-class detection.**

4️⃣ **Final Model**

Random Forest Classifier<br>
Produced high recall for failure detection

5️⃣ **Predictions & Export**

**Predicted machine failure labels for new input data and exported:**<br>
Predicted Machine Failure Results.csv

📊 **Results Summary**

**Metric score for Class 0 (no failure)** <br>
Precision-1.00<br>
Recall-0.98<br>
F1-score-1.00<br>

**Metric score for Class 1(Failure)**<br>
Precision-0.40<br>
Recall-0.83<br>
F1-score-0.54<br>

**Overall Accuracy:** 0.98<br>
**ROC–AUC (Test Set):** 0.96

**Although accuracy is high due to class imbalance, recall and F1-score were prioritized because missing a machine failure can be costly.
ROC–AUC Score: 0.96 → Demonstrates strong separability between failure and non-failure classes.**

🧠 **Insights from Feature Importance**

**Most influential parameters were:**<br>
Torque (Nm)<br>
Rotational speed (rpm)<br>
OSF (Overstrain Failure indicator)<br>
Tool wear (min)<br>
HDF (Heat Dissipation Failure indicator)<br>
TWF (Thermal Wear Failure indicator)<br>
PWF (Power Failure indicator)<br>
Temp_diff (Temperature difference between process & air)<br>
Air temperature (K)<br>
**These variables strongly contribute to predicting machine failures.**

🏁 **Conclusion**

**The final model is highly effective in predicting machine failures and can support industries in:** <br>
Reducing downtime<br>
Planning preventive maintenance<br>
Lowering operational risk<br>
Improving production efficiency<br>

🔮 **Future Enhancements**

Integrate with real-time sensor streaming<br>
Implement model monitoring for drift<br>
Deploy as an API for live predictions<br>

👤 **Author**

**Ganesh**<br>
Machine Learning & Data Science Enthusiast
