# 🧮 Preprocessing and Feature Scaling in Machine Learning

## ⚙️ **1. Preprocessing Overview**

Preprocessing is the stage where raw data is transformed into a form suitable for machine‑learning models.  
It ensures consistency, reduces noise, and improves model performance.

### **Common Steps**

- **Data Cleaning**
  - Handle missing values (imputation, removal).
  - Remove duplicates and outliers.
  - Correct inconsistent formats (e.g., date strings, categorical labels).

- **Data Transformation**
  - Encode categorical variables (one‑hot, label encoding).
  - Convert text to numerical form (TF‑IDF, embeddings).
  - Normalise numerical ranges.

- **Feature Engineering**
  - Create new features from existing ones.
  - Combine or split columns to reveal hidden relationships.
  - Apply domain knowledge to enrich the dataset.

- **Dimensionality Reduction**
  - Use PCA, t‑SNE, or autoencoders to reduce feature count.
  - Helps combat overfitting and improve interpretability.

---

## 📏 **2. Feature Scaling**

Feature scaling ensures that all numerical features contribute equally to the model’s learning process.  
Without scaling, features with large ranges can dominate gradient updates or distance calculations.

### **Why It Matters**

- Gradient‑based models (e.g., neural networks, logistic regression) converge faster when features are scaled.
- Distance‑based models (e.g., k‑NN, SVM, clustering) rely on comparable feature magnitudes.
- Regularisation terms (L1/L2) behave correctly only when features are on similar scales.

---

### **Common Scaling Techniques**

| Technique | Formula | Typical Use | Notes |
|------------|----------|--------------|-------|
| **Min‑Max Scaling** | \(x' = \frac{x - x_{min}}{x_{max} - x_{min}}\) | Neural networks, image data | Scales to [0, 1] or custom range |
| **Standardisation (Z‑score)** | \(x' = \frac{x - \mu}{\sigma}\) | Linear models, PCA | Centres at 0, unit variance |
| **Robust Scaling** | \(x' = \frac{x - \text{median}}{\text{IQR}}\) | Outlier‑heavy data | Less sensitive to extreme values |
| **Log Scaling** | \(x' = \log(x + 1)\) | Skewed distributions | Compresses large ranges |
| **Unit Vector Scaling** | \(x' = \frac{x}{\|x\|}\) | Text embeddings, cosine similarity | Normalises feature vectors |

---

## 🧠 **3. Practical Tips**

- Always **fit** your scaler on the training set and **apply** it to validation/test sets.
- Combine scaling with **pipeline objects** (e.g., `sklearn.pipeline.Pipeline`) to avoid data leakage.
- Visualise distributions before and after scaling to confirm transformations behave as expected.
