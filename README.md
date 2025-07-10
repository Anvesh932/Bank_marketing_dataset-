# Bank_marketing_dataset-
https://colab.research.google.com/drive/1SJ0sDGo8BSbs1q9qOveGJGXvJdaYK4RA?usp=sharing

#  Bank Marketing Prediction Project

##  Summary and Evaluation

The **Bank Marketing dataset** focuses on predicting whether a client will subscribe to a term deposit after a marketing phone call campaign. One of the main challenges identified during our **Exploratory Data Analysis (EDA)** was a significant **class imbalance**: most clients did not subscribe ("no"), while only a small fraction did ("yes"). Understanding this imbalance was critical, as it affects both the choice of metrics and the modeling strategy.

During EDA, we examined relationships between features and the target variable:
- Clients with **higher account balances** showed a slightly higher tendency to subscribe, suggesting socioeconomic influence.
- The **Job** feature revealed interesting patterns: professions like management and technician exhibited higher positive response rates.

Such insights can help inform targeted marketing strategies even before building predictive models.

---

##  Baseline Model

As a baseline, we implemented a **Logistic Regression** model. While it achieved high overall accuracy, it performed poorly in identifying the minority positive class ("yes"), which is crucial for marketing applications. Correctly identifying potential subscribers is far more valuable than merely achieving high accuracy on the majority "no" class.

---

##  Improvement Step

To address this, we applied a **class-weight balancing technique** in Logistic Regression. After this improvement:
- **AUC increased to 0.90**, indicating stronger separability.
- **F1 score for the positive class improved to 0.53**, indicating a better balance between precision and recall.

Although the overall accuracy slightly decreased, this trade-off is worthwhile to better detect potential subscribers.

---

##  What worked well

- Class weighting significantly improved minority class recall and F1 score.
- One-hot encoding preserved interpretability and allowed the Logistic Regression to work effectively.

---

##  What didn't work as well

- Overall accuracy dropped slightly, as expected when prioritizing the minority class.
- Logistic Regression may still lack the ability to capture complex non-linear relationships.

---

##  Future Directions

If more time were available, further improvements could include:
- Using ensemble methods such as **Random Forest** or **XGBoost** to capture non-linear interactions.
- Applying resampling techniques like **SMOTE** to balance the classes and improve minority class precision.
- Conducting feature engineering, e.g., creating interaction features or binning continuous variables, to enrich the feature set.

---

##  Conclusion

This project highlights the importance of tackling class imbalance in predictive modeling, especially for marketing applications where correctly identifying potential customers is crucial. The improved model can help marketing teams focus resources on clients most likely to subscribe, making campaigns more effective and cost-efficient.

---
