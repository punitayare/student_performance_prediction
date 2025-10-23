# Linear Regression – Questions & Answers

## 1. What assumptions does linear regression make?
Linear regression works best when a few key conditions are met:  
- **Linearity:** The relationship between your inputs (features) and the target should be roughly a straight line.  
- **Independence:** Each observation should be independent of the others.  
- **Homoscedasticity:** The errors (difference between actual and predicted values) should have similar variance across all predictions.  
- **Normality of Residuals:** The errors should be normally distributed.  
- **No Multicollinearity:** Features shouldn’t be too strongly correlated with each other.

---

## 2. How do you interpret the coefficients?
- A coefficient tells you **how much the target changes** when the feature increases by one unit, keeping everything else constant.  
- **Positive coefficient:** The target goes up as the feature goes up.  
- **Negative coefficient:** The target goes down as the feature goes up.  
Think of it like the slope of a line in simple linear regression—it shows the direction and strength of the relationship.

---

## 3. What is R² score and why is it important?
- R² (coefficient of determination) tells you **how much of the target’s variation is explained by your features**.  
- **Range:** 0 to 1 (closer to 1 is better).  
- Example: R² = 0.8 → Your features explain 80% of the variation in the target.  
- It’s a quick way to check how well your model fits the data.

---

## 4. When would you prefer MSE over MAE?
- **MSE (Mean Squared Error):** Squares errors, so it penalizes big mistakes more. Use it when you really want to avoid large errors.  
- **MAE (Mean Absolute Error):** Treats all errors equally. Better if you want a more “robust” measure and don’t care about a few big mistakes.  
- Bottom line: Choose MSE when big errors matter more.

---

## 5. How do you detect multicollinearity?
- **Correlation Matrix:** High correlations between features hint at multicollinearity.  
- **Variance Inflation Factor (VIF):** Values above 5–10 suggest trouble.  
- **Condition Number / Eigenvalues:** Very small eigenvalues or high condition number also indicate multicollinearity.  
Basically, it’s about checking if features are “too similar” to each other.

---

## 6. Difference between simple and multiple regression
- **Simple regression:** Only **one feature** predicts the target.  
 
- **Multiple regression:** Uses **two or more features**.  
  
- Multiple regression helps capture more complex relationships.

---

## 7. Can linear regression be used for classification?
- **Not really.** Linear regression predicts continuous values.  
- For classification problems (yes/no, categories), we use **logistic regression**, which is designed to predict probabilities.

---

## 8. What happens if you violate regression assumptions?
- **Linearity broken:** Predictions may be biased.  
- **Independence broken:** Confidence in your results goes down.  
- **Homoscedasticity broken:** Errors might be inconsistent, making predictions less reliable.  
- **Normality broken:** P-values and hypothesis tests might not be valid.  
- **Multicollinearity present:** Coefficients become unstable and hard to interpret.  

> In short: your model might still work, but the results could be misleading if assumptions aren’t met.
