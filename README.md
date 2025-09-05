### Name: Abhimanyu Vashishtha  
### Roll no: DA25C001
### The Assignment 2 is submitted in Assignment 2.ipnyb

## 📌 Project Overview
This project evaluates the impact of **Principal Component Analysis (PCA)** compared to a **Standardized Logistic Regression model** for classifying mushrooms as **edible** or **poisonous**.  
The dataset contains **23 categorical features**, which were one-hot encoded, creating redundancy and collinearity. PCA is applied to reduce dimensionality and handle correlated features effectively.

---

## ⚙️ Workflow

1. **Data Preprocessing**
   - One-hot encoding applied to categorical variables.  
   - Standardization performed to bring all features to equal variance.  

2. **Dimensionality Reduction (PCA)**
   - Scree plot shows that **58 PCs** are required to capture **95% variance**.  
   - PCA reduces redundant columns introduced by one-hot encoding.  

3. **Model Training**
   - Logistic Regression trained on:
     - **Standardized features** (full feature set).  
     - **PCA-reduced features** (lower-dimensional space).  

4. **Evaluation**
   - Metrics: Accuracy, Precision, Recall, F1-score.  
   - Visualization: Scatter plots & pair plots of principal components.  

---

## 📊 Results

### Classification Report (Standardized Model)

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.94      | 1.00   | 0.97     | 1828    |
| 1     | 1.00      | 0.81   | 0.90     | 609     |
| **Accuracy** |       |        | **95.3%** | 2437    |

---

### Classification Report (PCA Model)

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.92      | 1.00   | 0.96     | 1828    |
| 1     | 1.00      | 0.75   | 0.85     | 609     |
| **Accuracy** |       |        | **93.6%** | 2437    |

---

### Accuracy Comparison

| Model            | Accuracy |
|------------------|----------|
| PCA Model        | 93.6%    |
| Standardized     | 95.3%    |

---

## 🔎 Insights

- PCA reduced dimensionality by **removing redundant one-hot encoded features**.  
- Standardized model achieved slightly higher accuracy, but PCA performed nearly as well with **fewer features**.  
- PCA handled **feature collinearity** and redundancy effectively, offering computational efficiency.  
- Trade-off observed: PCA introduces minor **information loss**, but reduces **variance** and model complexity.  

---

## 📈 Visualizations

- **Scree Plot** → 58 PCs capture 95% variance.  
- **Scatter Plots (PC1 vs PC2)** → Good separability with some overlap.  
- **Pair Plots (PC1–PC5)** → Improved separability, reducing class confusion.  





# Run main script
python main.py
