# DA5401 A7: Multi-Class Model Selection using ROC and Precision-Recall Curves
**Name:** Samyam Rishika  
**Roll Number:** CE22B101  

---

## Project Overview
This project tackles the task of **multi-class land-cover classification** using **Landsat satellite imagery** from the **UCI Statlog (Landsat Satellite) dataset**.  
Each pixel in the dataset is described by **36 spectral bands**, and the objective is to assign each pixel to one of several **terrain or land-cover classes** such as soil, vegetation, or water.  

The project systematically evaluates multiple **machine learning models** including **KNN**, **SVM**, **Decision Tree**, **Naive Bayes**, **Logistic Regression**, and **Dummy Baseline** and later extends to **Random Forest** and **XGBoost** for ensemble comparison.  

Through comprehensive evaluation using **Accuracy**, **Weighted F1-Score**, **ROC-AUC**, and **Precision-Recall Average Precision (AP)**, the goal is to identify the model that offers the most **balanced and generalizable performance**.

---

## Folder Structure
```bash
├── assignment7.ipynb   # Main Jupyter Notebook (all code, plots, analysis, narrative)
└── README.md           # Project overview and execution guide
```
---

## How to Run
1. Clone the repository and navigate to the project directory:
   
```bash
git clone https://github.com/Rishika-28/assignment-7-Rishika-28.git
cd assignment-7-Rishika-28
```

2. Open the notebook:
jupyter notebook assignment7.ipynb

3. Run all cells sequentially. The notebook will:
   - Download and parse the **Landsat Satellite Dataset** from UCI.
   - Perform **data cleaning, normalization, and visualization**.
   - Train and evaluate multiple classifiers (KNN, SVM, Decision Tree, Naive Bayes, Logistic Regression, Dummy).
   - Compute **One-vs-Rest ROC** and **Precision-Recall Curves** for each model.
   - Compare model performance based on **Accuracy**, **F1**, **ROC-AUC**, and **mAP (mean Average Precision)**.
   - Extend analysis with **Random Forest** and **XGBoost** ensembles for performance benchmarking, and come up with a model whose AUC < 0.5

---

## Key Findings
- **KNN** achieved the best overall results with **Macro AUC = 0.980**, and **Macro AP = 0.921**, outperforming all other models.  
- **SVM** closely followed with comparable AUC but slightly lower precision–recall performance.  
- **Decision Tree** and **Naive Bayes** showed moderate results, while **Dummy (Prior)** performed at random baseline levels.  
- Ensemble methods (**XGBoost**, **Random Forest**) further improved robustness, confirming the benefit of non-linear and ensemble-based approaches for this dataset.

---

## Requirements
pip install pandas numpy scikit-learn matplotlib seaborn xgboost

---

## Notes
1. The dataset is automatically downloaded from the UCI Repository in the code.
3. The Brownie task is included as well.
