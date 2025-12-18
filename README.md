# Amazon Product Dataset Preprocessing



## Overview

This repository contains my Jupyter Notebook (`visualization.ipynb`) for the data preprocessing assignment on the Amazon product dataset (`amazon.csv`).

The notebook demonstrates a complete preprocessing pipeline, including data cleaning, feature engineering, aggregation, and categorical encoding.

## What I Have Done

- Loaded and explored the raw Amazon product dataset.
- Cleaned the data by:
  - Removing currency symbols (`₹`) and percentage signs (`%`).
  - Converting `discounted_price`, `actual_price`, `discount_percentage`, `rating`, and `rating_count` to proper numeric types.
  - Handled missing values and inconsistent entries.
- Performed feature engineering:
  - Extracted `main_category` from the hierarchical `category` column.
  - Created a `high_rating_flag` column (1 if rating > 4.0, else 0).
- Conducted aggregation and summary analysis:
  - Used `GroupBy` to compute category-wise statistics.
  - Created pivot tables to show average ratings per category.
  - Generated crosstabs to count high-rated products across categories.
- Applied categorical encoding:
  - Used **Label Encoding** on both `main_category` and full `category` columns.
  - Created a separate `df_encoded` DataFrame to keep the original data unchanged.
  - Explained why Label Encoding was chosen over One-Hot Encoding (due to high cardinality: 211 unique subcategories).
- Documented all steps with clear markdown explanations and code comments.
- Concluded that the dataset is now clean, structured, and ready for EDA, visualization, and predictive modeling.

## Files

- `visualization.ipynb` – The complete Jupyter Notebook with all code, outputs, and explanations.
- `amazon.csv` – The original dataset (raw Amazon product data).

## Requirements

- Python libraries: `pandas`, `numpy`, `scikit-learn`

## How to Run

1. Open the notebook in Jupyter:
   ```bash
   jupyter notebook visualization.ipynb
