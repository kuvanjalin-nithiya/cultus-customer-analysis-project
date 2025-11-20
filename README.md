# Exploratory Analysis of Synthetic Customer Spending Data

This project performs an exploratory data analysis (EDA) on a synthetic customer dataset containing numerical and categorical features.  
The goal is to understand spending behavior, detect outliers, and uncover relationships between variables using descriptive statistics and visualization.

---

## **1. Dataset Overview**

The dataset contains:

- **Age** (numerical)  
- **Income** (numerical)  
- **SpendingScore** (numerical)  
- **Segment** (categorical: Low / Middle / High)

A synthetic dataset is generated using NumPy with realistic statistical distributions (minimum 500 rows).

---

## **2. Data Cleaning**

The following steps were performed:

- Checked for missing values  
- Verified datatypes  
- Computed descriptive statistics (mean, median, standard deviation, quartiles)  
- Ensured dataset consistency

---

## **3. Visualizations Included**

### **A. Histogram – Spending Score**
Shows the distribution and spread of customer spending behavior.  
_File:_ `histogram_spending_score.png`

### **B. Box Plot – Income**
Identifies extreme values and potential outliers in income.  
_File:_ `boxplot_income.png`

### **C. Scatter Plot – Age vs Spending Score**
Reveals trends/correlations between customer age and spending score.  
_File:_ `scatter_age_spending.png`

---

## **4. Segment Analysis**

The average income for each segment was computed using group-by operations:


