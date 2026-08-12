# 📘 **Linear Regression & Ordinary Least Squares (OLS)**  

---

## 🧩 **1. What Linear Regression Is**

**Linear regression** is a statistical method used to model the relationship between:

- a **dependent variable** \( y \)  
- one or more **independent variables** \( x \)

The goal is to find a **straight line** (or hyperplane, if multiple variables) that best describes how \( y \) changes as \( x \) changes.

### The basic model (simple linear regression)

\[
y = \beta_0 + \beta_1 x + \varepsilon
\]

Where:

- \( \beta_0 \) = intercept  
- \( \beta_1 \) = slope  
- \( \varepsilon \) = error term (difference between predicted and actual values)

### Intuition

You’re trying to draw the “best‑fitting” straight line through a cloud of points.

---

## 📉 **2. What “Best‑Fitting” Means**

We want a line where the **predictions** are as close as possible to the **actual data**.

For each data point:
\[
\text{error} = y_{\text{actual}} - y_{\text{predicted}}
\]

But errors can be positive or negative, so we square them to avoid cancellation.

---

## 🧮 **3. Ordinary Least Squares (OLS)**

**Ordinary Least Squares** is the method used to find the line that minimises the **sum of squared errors**.

### The objective function

\[
\text{Minimize } \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
\]

OLS chooses \( \beta_0 \) and \( \beta_1 \) so that this sum is as small as possible.

### Why squared errors?

- Squaring makes all errors positive  
- Larger errors are penalised more heavily  
- It gives a smooth, differentiable function we can optimise analytically

---

## 📐 **4. The OLS Solution (Closed Form)**

OLS gives exact formulas for the slope and intercept.

### Slope

\[
\beta_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}
\]

### Intercept

\[
\beta_0 = \bar{y} - \beta_1 \bar{x}
\]

These formulas guarantee the line that minimises squared error.

---

## 📊 **5. Assumptions Behind OLS**

OLS works best when these assumptions hold:

- **Linearity** — relationship between variables is linear  
- **Independence** — observations don’t influence each other  
- **Homoscedasticity** — errors have constant variance  
- **Normality of errors** — errors are normally distributed  
- **No multicollinearity** (for multiple regression)

These assumptions ensure unbiased, efficient estimates.

---

## 🎯 **6. What OLS Gives You**

Once fitted, OLS provides:

- **Predictions**  
- **Residuals** (errors)  
- **Goodness‑of‑fit measures** like \( R^2 \)  
- **Estimated coefficients** \( \beta_0, \beta_1, \ldots \)  
- **Statistical tests** (t‑tests, F‑tests)

---

## 📝 **7. Summary**

Linear regression models a straight‑line relationship between variables, and Ordinary Least Squares finds the line that minimises the total squared difference between predicted and actual values.

---
