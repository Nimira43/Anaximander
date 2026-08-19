# 📘 Multiple Linear Regression

## 🎯 Overview

**Multiple Linear Regression (MLR)** models the relationship between a **dependent variable (Y)** and **two or more independent variables (X₁, X₂, …, Xₙ)**.  
It extends simple linear regression by allowing multiple predictors to contribute to the output.

MLR answers:

> **How does Y change when several X variables change simultaneously?**

---

## 🧮 General Equation

\[
y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_n x_n + \epsilon
\]

Where:

- **β₀** — intercept  
- **β₁ … βₙ** — coefficients (effect of each predictor)  
- **x₁ … xₙ** — independent variables  
- **ε** — error term (unexplained variation)

---

## 🔍 Interpretation of Coefficients

Each coefficient **βᵢ** represents:

> The expected change in Y for a 1‑unit increase in Xᵢ, **holding all other variables constant**.

This “holding constant” aspect is what makes MLR powerful — it isolates the effect of each variable.

---

## ⚙️ How the Model Learns (OLS)

MLR typically uses **Ordinary Least Squares (OLS)** to find the best‑fitting hyperplane.

OLS minimises:

\[
\sum (y_i - \hat{y}_i)^2
\]

The solution uses matrix algebra:

\[
\hat{\beta} = (X^T X)^{-1} X^T y
\]

Where **X** is the design matrix containing all predictors.

---

## 🧱 The Design Matrix

For n samples and p predictors:

\[
X =
\begin{bmatrix}
1 & x_{11} & x_{12} & \dots & x_{1p} \\
1 & x_{21} & x_{22} & \dots & x_{2p} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
1 & x_{n1} & x_{n2} & \dots & x_{np}
\end{bmatrix}
\]

- First column is all **1s** → intercept  
- Each row is one observation  
- Each column is one predictor  

---

## 📌 Assumptions of Multiple Linear Regression

### **1. Linearity**

Relationship between predictors and target is linear.

### **2. Independence**

Observations are independent of each other.

### **3. Homoscedasticity**

Constant variance of residuals.

### **4. Normality of Errors**

Residuals should be normally distributed.

### **5. No Multicollinearity**

Predictors should not be highly correlated with each other.

---

## ⚠️ Multicollinearity

Occurs when predictors are strongly correlated.

Problems:

- Coefficients become unstable  
- Hard to interpret variable importance  
- Inflated standard errors  

Detection:

- **Variance Inflation Factor (VIF)**  
- **Correlation matrix**  
- **Condition number**

Solutions:

- Remove correlated variables  
- Combine variables  
- Use regularisation (Ridge/Lasso)

---

## 📊 Model Evaluation Metrics

### **R² (Coefficient of Determination)**  

Proportion of variance explained by the model.

### **Adjusted R²**  

Corrects R² for number of predictors.

### **RMSE (Root Mean Squared Error)**  

Measures prediction error magnitude.

### **MAE (Mean Absolute Error)**  

Average absolute difference between actual and predicted values.

### **p‑values**  

Indicate whether each predictor is statistically significant.

---

## 🌍 Real‑World Examples

- Predicting house prices using size, location, number of rooms  
- Forecasting sales using advertising spend across multiple channels  
- Modelling medical outcomes using age, BMI, blood pressure  
- Predicting student performance using study hours, attendance, prior grades  

---

## 🧪 Example Interpretation

If:

\[
y = 2 + 0.8x_1 - 1.2x_2
\]

Then:

- **β₀ = 2** → baseline value  
- **β₁ = 0.8** → each 1‑unit increase in X₁ increases Y by 0.8  
- **β₂ = -1.2** → each 1‑unit increase in X₂ decreases Y by 1.2  

---

## 🔮 Why MLR Matters in Machine Learning

- Foundation for many advanced models  
- Fast and interpretable  
- Works well when relationships are roughly linear  
- Helps identify important predictors  
- Useful baseline model before trying more complex algorithms  
