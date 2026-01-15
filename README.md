Random Forest Pipeline for Mycotoxin Prediction Based on Diet

This repository contains R scripts for:

Estimating dietary exposure to mycotoxins using EFSA occurrence data and the FoodEx classification system

Predicting the presence of mycotoxins in biological samples using Random Forest models based on maternal dietary intake

🔍 Overview

The workflow consists of two linked components:

1️⃣ Dietary mycotoxin exposure estimation

FFQ food items are mapped to FoodEx classification levels (L1–L3)

EFSA occurrence data are used to estimate lower bound (LB), upper bound (UB), and midpoint (MID) exposure

Daily intake is calculated per participant and summarized at population level

2️⃣ Random Forest classification

Dietary exposure variables are used as predictors

Random Forest models classify presence/absence of individual mycotoxins

Model performance is evaluated and optimized using ROC-based methods

🧪 Data Inputs
Dietary data

FFQ-derived daily food intake (g/day) per participant

FoodEx classification mapping (L1–L3)

Mycotoxin data

Measured concentrations of mycotoxins in biological samples (e.g. breast milk, µg/L)

Example target variable:

mycotoxin_name <- "ennb1_ug_l"

📊 Dietary Exposure Estimation Outputs

The following Excel files are generated:

MAMI_FFQ_to_FoodEx.xlsx

Mapping table linking FFQ food items to FoodEx classification levels (L1–L3).

Exposure_matrix_FoodEx_L1.xlsx
Exposure_matrix_FoodEx_L2.xlsx
Exposure_matrix_FoodEx_L3.xlsx

Participant-level daily mycotoxin exposure estimates:

Lower bound (LB)

Upper bound (UB)

Midpoint (MID)

Calculated separately for each FoodEx level and food group.

Overall_population_mycotoxin_exposure.xlsx

Population-level summaries of total daily mycotoxin intake:

Median, Q1, Q3

Mean LB and UB

Stratified by mycotoxin and FoodEx level

🌲 Random Forest Modelling Pipeline

The Random Forest pipeline performs the following steps:

Preprocessing of dietary exposure variables (filtering and scaling)

Binary classification of mycotoxin presence/absence

Model training using Random Forest

Performance evaluation:

Accuracy

Sensitivity

Specificity

Balanced accuracy

ROC AUC

Optimization of classification thresholds using ROC analysis

Visualization of:

Feature importance

ROC curves

Performance metrics

Export of results to Excel and PNG formats

📦 Outputs

Excel files with model metrics and predictions

ROC curve plots

Variable importance plots

Dietary exposure matrices and population summaries

🧾 Notes

FoodEx level L3 provides the highest dietary resolution, while L1 is more conservative and less specific

Enniatin exposure estimates are available only at FoodEx L3, due to EFSA data availability

Lower and upper bound scenarios follow EFSA guidance for handling left-censored data

📚 Data Sources

Occurrence data were obtained from EFSA scientific opinions and associated datasets:

EFSA aflatoxin occurrence data (Zenodo)

EFSA enniatin and beauvericin occurrence data (Zenodo)

EFSA ochratoxin A occurrence data (Zenodo)
