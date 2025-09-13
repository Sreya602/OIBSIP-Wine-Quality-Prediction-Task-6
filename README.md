# 🍷 Wine Quality Prediction



---

## 📌 Project Overview
This project analyzes a **wine quality dataset** (1143 samples, 13 features) to predict wine quality based on chemical characteristics such as acidity, density, sulphates, and alcohol.  
We test three machine learning models — **Random Forest, SGD Classifier, and Support Vector Classifier (SVC)** — to evaluate their effectiveness.

---

## 📂 Dataset
- **Rows:** 1143  
- **Columns:** 13  
- **Target Variable:** `quality` (integer score, 3–8)  
- **Features:**  
  - **Chemical properties:** fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol  
  - **Identifier:** `Id` (not useful for prediction)

✅ No missing values.  
✅ Data ranges are reasonable but contain outliers.  

---

## 🔍 Exploratory Data Analysis
- Most wines fall into **medium quality range (5–6)**.  
- **Alcohol content:** Ranges from 8.4 to 14.9. Higher values generally correspond to better quality.  
- **Volatile acidity:** Higher values negatively affect wine quality.  
- **Sulphates:** Positive correlation with quality.  

---

## 🧹 Data Preprocessing
- Outliers handled using **z-score capping**.  
- Dropped `Id` column.  
- Scaled numerical features using **StandardScaler**.  
- Split into **Training (80%)** and **Testing (20%)** sets.  

---

## 🤖 Models Trained
1. **Random Forest Classifier** 🌲  
   - Handles non-linear relationships and interactions.  
   - Accuracy: **70.74%**  

2. **Stochastic Gradient Descent (SGD) Classifier** ⚡  
   - Efficient, lightweight, good for large datasets.  
   - Accuracy: **54.59%**  

3. **Support Vector Classifier (SVC)** 📈  
   - Works well with smaller datasets and clear class boundaries.  
   - Accuracy: **62.88%**  

---

## 📊 Results & Visualizations
### Model Accuracy Comparison
- Random Forest: **0.7074**  
- SVC: **0.6288**  
- SGD: **0.5459**

📌 Random Forest clearly outperformed the other models.

### Feature Importance (Random Forest)
Top predictors of wine quality:
1. **Alcohol** → Higher alcohol → Higher quality  
2. **Sulphates** → Positive effect on quality  
3. **Volatile acidity** → Negative effect on quality  

---

## 📝 Key Findings
- Random Forest achieved the **highest accuracy (~71%)**.  
- Alcohol and sulphates are the **strongest positive predictors** of wine quality.  
- Volatile acidity is a **negative predictor** (higher acidity lowers quality).  
- SGD performed poorly, showing linear models may not capture complex interactions.  

---

## 🚀 Conclusion & Future Work
- **Best Model:** Random Forest (balanced accuracy and interpretability).  
- **Practical Insights:**  
  - Increase alcohol and sulphates for better wine quality.  
  - Control volatile acidity to avoid lower scores.  
- **Next Steps:**  
  - Hyperparameter tuning for Random Forest.  
  - Try Gradient Boosting or XGBoost for potentially higher accuracy.  
  - Explore regression framing (predict exact score) vs. classification.  

---
