
# Random Forest Pipeline for Mycotoxin Prediction Based on Diet

---

## 📌 Overview

This repository contains R scripts for:

- Estimating dietary exposure to mycotoxins using EFSA occurrence data and FoodEx classification
- Predicting the presence of mycotoxins in biological samples using Random Forest models
## 🔍 Workflow Overview

> ### 1️⃣ Dietary Mycotoxin Exposure Estimation
> - FFQ food items are mapped to FoodEx classification levels (L1–L3)
> - EFSA occurrence data are used to estimate:
>   - Lower bound (LB)
>   - Upper bound (UB)
>   - Midpoint (MID)
> - Daily intake is calculated per participant and summarized at population level
> ### 2️⃣ Random Forest Classification
> - Dietary exposure variables are used as predictors
> - Random Forest models classify presence/absence of individual mycotoxins
> - Model performance is evaluated and optimized using ROC-based methods
<details>
<summary><strong>📦 Dietary Mycotoxin Exposure Estimation</strong></summary>

- FFQ food items mapped to FoodEx classification levels (L1–L3)
- EFSA occurrence data used to estimate LB, UB, and MID exposure
- Daily intake calculated per participant and summarized at population level

</details>
<details>
<summary><strong>🌲 Random Forest Classification</strong></summary>

- Dietary exposure variables used as predictors
- Models classify presence/absence of individual mycotoxins
- Performance evaluated using ROC-based methods

</details>
## 🧩 Workflow Components

| Step | Component | Description |
|-----:|-----------|-------------|
| 1 | Dietary exposure estimation | FoodEx mapping + EFSA occurrence data (LB, UB, MID) |
| 2 | Random Forest modeling | Classification of mycotoxin presence using dietary predictors |
## 🔬 Workflow

> ### 1️⃣ Dietary Mycotoxin Exposure Estimation
> - FoodEx classification (L1–L3)
> - EFSA occurrence data
> - Population-level intake summaries

---

> ### 2️⃣ Random Forest Classification
> - Dietary predictors
> - Presence/absence classification
> - ROC-based optimization
