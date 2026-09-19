# ClinVar Genomic Variant Pathogenicity Classifier

An end-to-end Machine Learning pipeline predicting whether genomic variants are **Pathogenic** or **Benign** using the ClinVar dataset.

## Project Summary
- **Model:** Random Forest Classifier (`class_weight='balanced'`)
- **Key Metric:** Class 1 (Pathogenic) Recall = 0.75
- **Goal:** Prioritize high sensitivity (Recall) to minimize False Negatives in clinical variant screening.

## Pipeline Steps
1. Data Cleaning & Median Imputation
2. One-Hot Encoding categorical nucleotide features (`REF`, `ALT`)
3. Stratified Train/Test Split (80/20) & `StandardScaler`
4. Baseline Logistic Regression vs. Optimized Random Forest
5. Threshold Adjustment ($0.35$) for high pathogenic recall

## Dependencies
- `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`
