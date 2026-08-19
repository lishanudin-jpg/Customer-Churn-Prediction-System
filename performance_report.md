# Customer Churn Prediction System — Performance Report

## 1. Objective
Build a classification model that predicts whether a customer is likely to churn and assigns a customer risk level.

## 2. Dataset
The project uses a synthetic dataset containing 1,200 customer records.

The target variable is `Churn`:
- 0 = Customer stays
- 1 = Customer churns

## 3. Preprocessing
- Customer ID removed from model features.
- Missing numerical values filled using median imputation.
- Missing categorical values filled using most-frequent imputation.
- Categorical variables encoded using One-Hot Encoding.
- Numerical variables standardized.
- Data split using 80% training and 20% testing with stratification.

## 4. Models
The notebook compares:
1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Gradient Boosting

Random Forest is used as the final model.

## 5. Final Model Performance

| Metric | Score |
|---|---:|
| Accuracy | 0.8583 |
| Precision | 0.8805 |
| Recall | 0.9660 |
| F1 Score | 0.9213 |
| ROC-AUC | 0.7636 |

## 6. Confusion Matrix

```text
                 Predicted
              No Churn   Churn
Actual No            7      27
Actual Churn         7     199
```

## 7. Business Use
The system can help identify customers who may require retention attention. High-risk customers can be prioritized for support, service review, renewal communication, or suitable retention programs.

## 8. Risk Classification
- Low Risk: churn probability < 30%
- Medium Risk: 30% to < 70%
- High Risk: >= 70%

## 9. Limitations
The dataset is synthetic. Results should not be treated as real-world business performance. A prediction is a probability, not a guarantee.

## 10. Future Enhancements
- Streamlit prediction interface
- Hyperparameter tuning
- Cross-validation
- SHAP explainability
- Real customer dataset
- Model monitoring and retraining
- Automated retention recommendations

## 11. Conclusion
The project demonstrates a complete machine learning workflow from data preprocessing to classification, evaluation, feature analysis, customer risk prediction, and trained-model persistence.
