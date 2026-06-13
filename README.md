# AI-Powered E-commerce Order Status Prediction System

## Problem Statement

The objective of this project is to predict the final status of an e-commerce order using machine learning.

Target Classes:
- Shipped_Done
- Cancelled
- Problem_Pending

The project helps identify orders that are likely to be cancelled or face delivery issues.

---

## Dataset

The dataset contains more than 120,000 e-commerce order records.

Features used:
- Fulfilment
- Sales Channel
- Category
- Size
- ship-city
- ship-state
- ship-postal-code
- B2B
- Week
- Style_Group
- ship-service-level

Target:
- Status_Group

---

## Data Preprocessing

Steps performed:

- Missing value handling
- Feature engineering
- Status grouping
- Categorical encoding
- Leakage detection

---

## Target Engineering

Original order statuses were grouped into:

| Original Status | Status_Group |
|----------------|-------------|
| Shipped | Shipped_Done |
| Delivered to Buyer | Shipped_Done |
| Cancelled | Cancelled |
| Returned / Pending / Lost | Problem_Pending |

---

## Models Used

- Random Forest Classifier
- XGBoost Classifier

---

## Leakage Analysis

Initial models achieved more than 98% accuracy.

Feature importance analysis revealed that:

- Courier Status
- Qty
- Amount

introduced target leakage.

A more realistic model was built after removing these features.

---

## Final Results

- Accuracy: 93.33%
- Weighted F1 Score: 92.71%

The model successfully predicts order outcomes using operational and order-related information.

---

## Key Insights

- Fulfilment method affects order outcomes.
- Sales channels influence shipment success.
- Weekly patterns impact order status.
- Location-based features contribute to delivery performance.

---

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost

---

## Project Structure

```text
ecommerce-order-status-prediction/
│
├── data/
├── notebooks/
├── images/
└── README.md
```
