# README

## Dengue Hematological Dataset (Bangladesh) - ML Analysis

This project analyzes the Dengue Hematological Dataset collected from Jamalpur 250-Bed General Hospital, Bangladesh (Feb 10, 2024 – Sep 27, 2024). It contains 1,523 patient records with demographic and hematological features relevant to dengue diagnosis.

---

## 📂 Dataset Details

- **Records:** 1,523 patients
- **Features:** 19 columns (demographics + hematological parameters)
- **Target:** Dengue Test Result (Positive / Negative)
- **Source:** [Mendeley Data](https://data.mendeley.com/datasets/6fsrsk3mb8/2)

### Features

- **Demographics:** Age, Gender
- **Hematological Parameters:** Hemoglobin, RBC, WBC, Neutrophils, Lymphocytes, Monocytes, Eosinophils, Basophils, Platelet count, MCV, MCH, MPV, PDW, etc.

---

## 📊 Workflow Overview

1. **Data Loading & Exploration**
   - Load CSV using pandas.
   - Display info, summary statistics, and check for missing values.

2. **Visualization**
   - Distribution plots for target and key features.
   - Correlation heatmaps and boxplots for outlier detection.

3. **Preprocessing**
   - Label encoding for categorical variables (`Gender`, `Result`).
   - Outlier treatment using IQR clipping.
   - Standardization of numerical features.

4. **Feature Engineering**
   - Creation of hematological ratios: NLR, PLR, MLR, MPV/PLT, PDW/PLT.

5. **Train-Test Split**
   - 80/20 split with stratification on the target.

6. **Modeling Pipeline**
   - Handle class imbalance with SMOTE.
   - Models: RandomForest, LogisticRegression, XGBoost.
   - Hyperparameter tuning with GridSearchCV and Stratified K-Fold CV.
   - Evaluation using F1-score, accuracy, ROC-AUC, and classification report.

---

## 🛠️ How to Run

1. **Requirements**
   - Python 3.x
   - pandas, numpy, matplotlib, seaborn
   - scikit-learn, imbalanced-learn, xgboost

2. **Steps**
   - Place the dataset CSV in `Dataset/`.
   - Open and run the notebook: [NotebookFile/main.ipynb](NotebookFile/main.ipynb).

---

## 📈 Use Cases

- Dengue diagnosis prediction models
- Severity classification based on blood parameters
- Biostatistical analysis of hematological changes in dengue patients
- Educational use for ML in healthcare research
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->


---

## 📄 File Structure

```
Dataset/
    Dengue Fever Hematological Dataset.csv
NotebookFile/
    main.ipynb
```

---

## 🔗 Reference

- [Mendeley Data – Dengue Hematological Dataset (Bangladesh)](https://data.mendeley.com/datasets/6fsrsk3mb8/2)