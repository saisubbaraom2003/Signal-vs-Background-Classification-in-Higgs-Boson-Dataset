# Higgs Boson Classification Challenge (Kaggle)

## 📌 Project Overview
This project focuses on the **Higgs Boson Machine Learning Challenge**, hosted on [Kaggle](https://www.kaggle.com/c/higgs-boson).  
The task is to **classify particle collision events** as either:
- **Signal (`s`)**: Events resembling Higgs boson decay  
- **Background (`b`)**: Events from other physics processes  

The dataset was simulated by the **ATLAS experiment at CERN**.  

---

## 📂 Dataset
- **Size**: 250,000 training events, 32 features after cleaning  
- **Features**: Kinematic & particle physics properties  
- **Target**: Binary classification → `s` (signal) or `b` (background)  
- **Special Notes**: `-999` indicates missing values  

---

## ⚙️ Data Preprocessing
- Dropped **EventId** (non-predictive column)  
- Replaced `-999` with **NaN**  
- Removed features with **>70% missing values**  
- Outlier treatment using **IQR method**  
- Reduced skewness with **PowerTransformer (Yeo-Johnson)**  
- Removed multicollinearity via **VIF analysis**  

---

## 🤖 Model Building
- Model: **XGBoost Classifier**  
- Why XGBoost?  
  - Handles non-linearity & missing values well  
  - Regularization to prevent overfitting  
  - Widely successful in Kaggle competitions  

---

## 📊 Results
- **Accuracy**: 100%  
- **F1 Score**: 1.0  
- **ROC-AUC**: 1.0  
- **Cross-validation (5 folds)**: Mean = 1.0  

### Visuals
- Confusion Matrix ✅  
- ROC Curve ✅  

---

## 🛠 Tech Stack
- **Language**: Python  
- **Libraries**: Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn  

---

## 🚀 Future Work
- Evaluate models using **AMS (Approximate Median Significance)** metric  
- Experiment with **deep learning models (e.g., MLP, CNN on features)**  
- Apply techniques to **real-world noisy physics datasets**  

---

## 👨‍💻 Author
Project developed by *Sai Subba Rao Mahendrakar*  

---
