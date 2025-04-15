# 🧠 Supervised Learning on Chocolate & Mushroom Datasets

**Course:** CSI5155 - Fall 2024  
**Author:** Vrishab Prasanth Davey  
**Student ID:** 300438343  

## 📌 Overview

This project evaluates six supervised learning models on two datasets—one imbalanced (Chocolate) and one balanced (Mushroom). Models were tested using four approaches:  
- **No Rebalancing**  
- **Undersampling**  
- **Oversampling (SMOTE)**  
- **Combined Sampling**  

Performance was analyzed using **AUC**, **precision**, **recall**, and **F1-score**.

---

## 📊 Models Used
- Decision Tree  
- Random Forest  
- SVM  
- Gradient Boosting  
- MLP (Multi-Layer Perceptron)  
- k-NN  

---

## 🍫 Chocolate Dataset (Imbalanced)

### 🔹 No Rebalancing:
- **Best Model:** Gradient Boosting (AUC = 0.75)  
- **Worst AUC:** SVM (0.19), MLP (0.24)  
- **Observation:** High F1-scores (~0.99) but poor AUC due to predicting only the majority class.

### 🔹 Undersampling:
- Improved AUC for SVM and MLP (0.42 and 0.46)  
- Gradient Boosting and Decision Tree AUC dropped  
- Tradeoff: Higher recall, but lower accuracy

### 🔹 Oversampling (SMOTE):
- **Best AUC:** MLP (AUC = 0.70)  
- Higher F1 scores  
- Risk of overfitting, especially for ensemble models

### 🔹 Combined Sampling:
- Mixed performance with most models  
- MLP retained high F1 (0.95)  
- Decision Tree and Random Forest saw performance drops due to noise

---

## 🍄 Mushroom Dataset (Balanced)

### 🔹 No Rebalancing:
- High AUC values across all models  
- **Best Models:** SVM, Random Forest (AUC = 0.83)  
- Consistent performance with recall and F1-score between 0.65–0.70

### 🔹 Undersampling:
- No major drop in performance  
- Maintained high recall; dataset was already balanced

### 🔹 Oversampling:
- AUC dropped for some models due to synthetic noise  
- **Good Performance:** Random Forest, MLP, k-NN (AUC = 0.75–0.77)  
- Gradient Boosting overfitted (AUC = 0.75)

### 🔹 Combined Sampling:
- **Low AUC:** Decision Tree (0.64)  
- Other models remained robust (AUC = 0.80–0.82)  
- SVM and RF showed resilience to sampling noise

---

## ✅ Conclusion

- **Chocolate Dataset:** Benefited most from oversampling  
- **Mushroom Dataset:** Performed well across all strategies  
- **Top Performers:** SVM and MLP (robust across datasets and sampling strategies)  
- **Challenging Models:** Random Forest & Gradient Boosting struggled with synthetic data; Decision Tree highly sensitive to noise  
- **k-NN:** Stable across all resampling techniques  

> 🔁 As discussed in lectures, there is no one-size-fits-all “ideal” model. Dataset distribution and model robustness to noise must guide method selection — echoing the "No Free Lunch" theorem.

---
