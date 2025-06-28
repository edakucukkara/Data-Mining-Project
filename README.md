# 🛍️ Predicting Customer Repurchase Behavior in E-Commerce

This project applies **predictive analytics** to anticipate customer repurchase behavior in the context of **fast-moving consumer goods (FMCG)** on an e-commerce platform. By analyzing historical transaction data and product attributes, we build a machine learning model capable of predicting whether a customer will reorder a product within a 4-week timeframe. Our results demonstrate how **Random Forest** outperforms other models like **XGBoost** and **Logistic Regression** in terms of accuracy and robustness.

---

## 🔍 Problem Statement

Can we predict **if a customer will repurchase a product in the next 28 days**?

This capability is highly relevant for:

- Personalized product replenishment suggestions  
- Optimized inventory and supply chain planning  
- Improved customer satisfaction and retention

---

## 📊 Dataset Overview

| File                     | Description                                          |
|--------------------------|------------------------------------------------------|
| `transactions.csv`       | Contains customer ID, product ID, purchase date, and quantity |
| `product_catalog.csv`    | Metadata such as product name, brand, and attributes |
| `product_category_map.csv` | Category relationships (e.g., category, subcategory) |
| `test.csv`               | Dataset for evaluating final model performance       |

---

## 🛠️ Preprocessing & Feature Engineering

Key transformations include:

- Datetime parsing and sliding window generation  
- Category explosion for hierarchical mapping  
- Label encoding for categorical variables  
- Missing value imputation (zero or `"Unknown"`)  
- Feature generation: recency, frequency, average quantity, purchase intervals

---

## 🤖 Models Evaluated

Three models were compared:

| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| **Random Forest**   | 86%      | 86%       | 86%    | 86%      |
| XGBoost             | 46%      | 46%       | 46%    | 45%      |
| Logistic Regression | 27%      | 26%       | 27%    | 23%      |

**Conclusion**: Random Forest achieved the best balance between accuracy, recall, and precision. SMOTE was used to handle class imbalance.

---

## 📈 Results

- ✅ Random Forest delivered high generalization and stability across all classes  
- 📉 Confusion matrices confirmed balanced performance and minimized misclassifications  
- ❌ XGBoost and Logistic Regression struggled with imbalanced data and non-linear relationships

---

## 📌 Key Contributions

- ✅ Real-world data preprocessing pipeline  
- ✅ Feature engineering for purchase behavior  
- ✅ Model comparison: ensemble vs linear vs boosting  
- ✅ Handling class imbalance with SMOTE  
- ✅ Final model achieving **86% balanced accuracy**

---
