# Chest Pain during Panic Attack

## 📌 Project Overview
This project aims to classify whether an individual is experiencing Chest_Pain during panic attack based on tabular data containing medical and behavioral features. The dataset consists of multiple features, but most of them have **low correlation with the target variable**, which affects model performance.

## 📂 Dataset Details
- Number of samples: **1200**
- Number of features: **18**
- Target Variable: **Chest_Pain**
- Features:  
  - **Panic_Attack_Frequency**  
  - **Duration_Minutes**  
  - **Trigger**  
  - **Heart_Rate**  
  - **Sweating**  
  - **Shortness_of_Breath**  
  - **Dizziness**  
  - **Chest_Pain**  
  - **Trembling**  
  - **Medical_History**  
  - **Medication**  
  - **Caffeine_Intake**  
  - **Exercise_Frequency**  
  - **Sleep_Hours**  
  - **Alcohol_Consumption**  
  - **Smoking**  
  - **Therapy**  
  - **Panic_Score**  
- Notable Feature Correlation: **Most features have 0.000 correlation, while a few have values ranging from 0.05 to 0.6.**

## 🔧 Preprocessing Steps
- **Handled missing values** using `SimpleImputer`
- **Feature transformation** using `ColumnTransformer`
- **Data balancing** attempted with `SMOTE` (but results remained suboptimal)
- **Feature scaling** applied where necessary

## 🏆 Models Used & Accuracy
| Model                     | Accuracy |
|---------------------------|----------|
| XGBoost Classifier       | 0.56     |
| Bagging Classifier       | 0.566    |
| Random Forest Classifier | 0.58     |

### 🔍 Key Findings
- **Low accuracy is due to weak feature correlation** with the target variable.
- **Even ensemble models like XGBoost and RandomForest did not significantly improve results.**
- **Feature engineering did not lead to major accuracy improvements.**

## 📌 Repository Link
GitHub: [Panic Attack Classification](https://github.com/SadabAli/Panic-Attack.git)

## ⚡ Conclusion
This project highlights the challenges of working with datasets where features have weak relationships with the target variable. Despite using **ensemble methods and hyperparameter tuning**, the **maximum accuracy achieved was 58%**. Future work could involve **feature engineering** or **collecting better-quality data** to improve performance.
