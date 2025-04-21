# Random Forest Pipeline for Mycotoxin Prediction Based on Diet

This repository contains an R script implementing a full Random Forest classification pipeline to predict the presence of specific mycotoxins in human samples based on maternal dietary intake data.

---

## 🔍 Overview

The pipeline:
- Preprocesses dietary data (scaling and filtering)
- Builds Random Forest models to classify presence/absence of each mycotoxin
- Evaluates model performance using accuracy, sensitivity, specificity, AUC, and balanced accuracy
- Optimizes classification thresholds using ROC analysis
- Visualizes feature importance and performance metrics
- Exports all results to Excel and PNG format

---

## 🧪 Data Inputs

- `X`: a scaled matrix or dataframe of dietary intake variables
- `x_data_clean`: a dataframe containing mycotoxin concentrations (ug/L) per sample

Example target:
```r
mycotoxin_name <- "ennb1_ug_l"

