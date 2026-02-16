# Census Data Analysis - README

**Project:** Take Home Assignment  
**Author:** Shivani Madan  
**Email:** shivanimadan1099@gmail.com

---

## Project Overview

This project contains two main analyses on US Census Bureau income data:

1. **Task 1:** Income Classification (Binary prediction: <$50K vs ≥$50K)
2. **Task 2:** Customer Segmentation for targeted marketing

---

## Project Structure
project/
│
├── Task1_final.ipynb          # Income classification analysis
├── Task2_final.ipynb           # Customer segmentation analysis
├── census-bureau.data              # Raw dataset
├── census-bureau.columns           # Column names file
├── after_feature_engineering.csv   # Preprocessed data (generated)
├── README.md                       # This file
---

## Requirements

### **Python Version**
- Python 3.8 or higher

### **Required Libraries**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy
```
Or install all at once:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy jupyter
```


### **How to Run**
**Option 1: Jupyter Notebook (Recommended)**

Install Jupyter:

    pip install jupyter

Launch Jupyter:

```bash
jupyter notebook
```

Open and run:

    Open Task1_final.ipynb for classification

    Open Task2_final.ipynb for segmentation

    Click Cell → Run All or run cells sequentially

**Option 2: Command Line Execution**

Convert notebooks to Python scripts:

```bash
    jupyter nbconvert --to script Task1_final.ipynb
    jupyter nbconvert --to script Task2_final.ipynb
```
Run scripts:

```bash
python Task1_final.py
python Task2_final.py
```

### **Task 1: Income Classification**
What it does:

    -> Predicts whether individuals earn >$50K or <$50K annually
    
    -> Uses XGBoost classifier with hyperparameter tuning
    
    -> Handles severe class imbalance (15:1 ratio)

Key Outputs:
    
    Model Accuracy: 95% (with optimal threshold 0.85)

    ROC-AUC Score: 0.9490

Run Time: ~ 5-10 minutes

### **Task 2: Customer Segmentation**
What it does:
    
    -> Groups census population into 4 distinct customer segments

    -> Uses K-Means clustering with PCA dimensionality reduction

    -> Provides marketing strategies for each segment

Key Outputs:
    4 Customer Segments:

    Segment 0: Young Professionals (7.6%)

    Segment 1: Senior Citizens (20.7%)

    Segment 2: Children & Minors (27.5%)

    Segment 3: Established Families (44.1%)

Run Time: ~3-5 minutes

### **Data Files**
Input Files (Required):

    census-bureau.data - Raw census data (199,523 rows)

    census-bureau.columns - Column names
    
    Note: Place these files in the same directory as notebooks

Generated Files:

    after_feature_engineering.csv - Created by Task 1, used by Task 2

Additional File - Project Report


## **Troubleshooting**
Common Issues:
1. Import Error: No module named 'xgboost'

```bash
pip install xgboost
```
2. File Not Found: census-bureau.data

```bash
Ensure data files are in the same directory as notebooks
```

3. Memory Error
```bash
Reduce sample size or use a machine with more RAM (dataset is ~200K rows)
```
4. Plots not displaying