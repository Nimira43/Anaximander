# 📘 Polynomial Regression

Polynomial Regression is an extension of linear regression that allows the model to fit **curved relationships** between the independent variable(s) and the dependent variable.

It does this by adding **polynomial terms** (powers of X) to the regression equation, enabling the model to capture non‑linear patterns while still remaining *linear in the parameters*.

---

## 🎯 Why Polynomial Regression?

Polynomial regression is used when:

- The relationship between X and Y is **non‑linear**  
- A straight line (simple linear regression) **underfits** the data  
- You want a flexible model without moving to more complex ML algorithms  
- You need interpretable coefficients but with curved behaviour  

It is especially useful for:

- Growth curves  
- Trend modelling  
- Physics/engineering relationships  
- Economics and forecasting  
- Any dataset where the pattern bends or curves  

---

## 🧮 The Polynomial Regression Equation

### **General Form**

For a polynomial of degree *d*:

\[
y = \beta_0 + \beta_1 x + \beta_2 x^2 + \beta_3 x^3 + \dots + \beta_d x^d + \epsilon
\]

Where:

- **β₀** — intercept  
- **β₁, β₂, … β_d** — coefficients for each polynomial term  
- **x, x², x³, … xᵈ** — polynomial features  
- **ε** — error term  

Even though the equation contains powers of X, the model is still **linear in the parameters β**, which means:

- It can be solved using **Ordinary Least Squares (OLS)**  
- It behaves like linear regression with transformed features  

---

## 🔧 How It Works (Feature Expansion)

Polynomial regression does not change the underlying regression algorithm — it changes the **input features**.

Example:  
If your original feature is:

\[
x = [1, 2, 3]
\]

A degree‑3 polynomial expansion becomes:

| x | x² | x³ |
|---|----|----|
| 1 | 1  | 1  |
| 2 | 4  | 8  |
| 3 | 9  | 27 |

These expanded features are then fed into a standard linear regression model.

---

## 📈 Visual Intuition

- **Degree 1:** straight line  
- **Degree 2:** parabola (U‑shape or inverted U)  
- **Degree 3:** S‑curve  
- **Higher degrees:** increasingly flexible curves  

Higher degrees can fit complex patterns — but at a cost.

---

## ⚠️ Overfitting Risk

Polynomial regression is powerful but can easily overfit, especially with high degrees.

### Signs of overfitting

- Model fits training data perfectly  
- Wild oscillations between data points  
- Poor generalisation to new data  

### Ways to reduce overfitting

- Use cross‑validation  
- Limit polynomial degree  
- Use regularisation (Ridge, Lasso)  
- Use domain knowledge to choose degree  

---

## 📌 Choosing the Degree

There is no universal rule — but common practice includes:

- Start with **degree 2 or 3**  
- Use **validation error** to choose the best degree  
- Avoid very high degrees unless justified  
- Visualise the fitted curve  

---

## 🧪 Example Interpretation

For a degree‑2 model:

\[
y = \beta_0 + \beta_1 x + \beta_2 x^2
\]

- **β₁** controls the linear trend  
- **β₂** controls the curvature  
- Positive β₂ → U‑shape  
- Negative β₂ → inverted U  

---

## 📊 Advantages

- Simple to implement  
- Works with OLS  
- Captures non‑linear patterns  
- Still interpretable  
- Fast to train  

---

## 📉 Disadvantages

- Sensitive to outliers  
- High-degree polynomials can behave erratically  
- Overfitting risk increases with degree  
- Extrapolation becomes unreliable  

---

## 🌍 Real‑World Uses

- Modelling temperature curves  
- Predicting population growth  
- Economics demand curves  
- Engineering stress/strain relationships  
- Trend forecasting in time series  

---

## 🧠 Key Takeaways

- Polynomial regression = linear regression with polynomial features  
- Great for modelling curved relationships  
- Degree selection is crucial  
- Beware of overfitting  
- Still solved using OLS  
