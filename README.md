# Building-Energy-Load-Prediction
# 📊 Perbandingan Kinerja Algoritma Linear Regression, Random Forest, dan Support Vector Regression dalam Prediksi Konsumsi Energi Bangunan Berdasarkan Karakteristik Desain

## 📌 Overview
Pengembangan model Machine Learning untuk memprediksi beban pemanasan dan pendinginan (Heating &amp; Cooling Load) bangunan. Dengan membandingkan kinerja algoritma Linear Regression, Random Forest, dan Super Vector Regression  

Pendekatan yang digunakan adalah dengan membandingkan kinerja tiga algoritma regresi:
- Linear Regression (Ridge)
- Random Forest
- Support Vector Regression (SVR)

Tujuan utama adalah menemukan model terbaik dalam memprediksi konsumsi energi bangunan berdasarkan karakteristik desainnya.

## 📂 Dataset
Dataset yang digunakan adalah **Energy Efficiency Dataset (ENB2012_data)**:  
👉 https://www.kaggle.com/datasets/elikplim/eergy-efficiency-dataset/data  

### 🧾 Deskripsi Dataset
Dataset ini dibuat oleh **Angeliki Xifara** dan diproses oleh **Athanasios Tsanas** (University of Oxford).  

Dataset digunakan untuk analisis energi pada **12 bentuk bangunan** yang disimulasikan menggunakan software Ecotect. Variasi bangunan didasarkan pada:
- Glazing Area (luas kaca)
- Distribusi kaca
- Orientasi bangunan
- Parameter desain lainnya  

Dataset terdiri dari:
- 768 data bangunan  
- 8 fitur (X1–X8)  
- 2 target (Y1 & Y2)  

### 🔍 Fitur
- X1: Relative Compactness  
- X2: Surface Area  
- X3: Wall Area  
- X4: Roof Area  
- X5: Overall Height  
- X6: Orientation  
- X7: Glazing Area  
- X8: Glazing Area Distribution  

### 🎯 Target
- Y1: Heating Load  
- Y2: Cooling Load  

## ⚙️ Metodologi

### 1. Data Preprocessing
- Handling missing values (median imputation)  
- Menghapus data duplikat  
- Outlier handling (IQR / Winsorization)  
- One-Hot Encoding untuk fitur kategorikal  

### 2. Data Splitting
- 70:30  
- 80:20  
- 90:10  

### 3. Model yang Digunakan
- Ridge Regression  
- Random Forest  
- Support Vector Regression (SVR)  

### 4. Evaluasi Model
Menggunakan metrik:
- RMSE  
- MAE  
- R² Score  

### 5. Hyperparameter Tuning
- GridSearchCV  
- 5-Fold Cross Validation  

## 📊 Hasil

### 🏆 Model Terbaik (Berdasarkan R² Score)

- **Heating Load (Y1)**  
  → Random Forest (Split 90:10)  
  → R² = **0.9979**

- **Cooling Load (Y2)**  
  → Random Forest (Split 70:30)  
  → R² = **0.9616**
