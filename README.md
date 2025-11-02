Feature Engineering on BMW Sales Dataset (2010–2024)
📘 Overview

This project demonstrates how to apply Feature Engineering techniques to transform raw automobile sales data into meaningful features using the BMW Sales Dataset (2010–2024).
The dataset includes information such as model, region, fuel type, price, mileage, and yearly sales figures. It can be used for predictive tasks such as sales forecasting, price estimation, and market trend analysis.

🧠 Feature Engineering Steps

1. Data Cleaning

Checked the dataset for missing values and inconsistencies.

Replaced missing numerical values (e.g., Price_USD, Mileage_KM) with the mean of their respective columns.

Filled missing categorical values (e.g., Region, Fuel_Type, Color) with the mode.

Ensured logical consistency for numeric data (e.g., Year between 2010–2024).

2. Encoding

Identified all categorical columns (Model, Region, Color, Fuel_Type, Transmission).

Applied One-Hot Encoding using pd.get_dummies() to convert them into numerical form suitable for model input.

3. Feature Scaling

Used StandardScaler to normalize numerical columns such as Price_USD, Mileage_KM, Engine_Size_L, and Sales_Volume.

This step ensures that all features contribute equally and prevents large-scale features from dominating.

4. Feature Extraction (PCA)

Applied Principal Component Analysis (PCA) with 2 components to visualize the data distribution and identify the most influential directions of variance.

The PCA scatter plot shows that the top two components capture most of the variability, reducing dimensionality effectively.

5. Feature Selection

Used Variance Threshold to remove low-variance and redundant features.

Applied SelectKBest (f_regression) to select the top 5 features most strongly correlated with Sales_Volume.

📊 Tools and Libraries

Python

pandas, numpy

scikit-learn

matplotlib, seaborn

⚖️ Ethical Considerations

Although the dataset does not contain personal information, fairness and transparency were maintained during feature processing.
To ensure ethical analysis:

Avoided biased or irrelevant attributes that could distort outcomes.

Used transparent preprocessing and scaling steps.

Ensured that all data transformations are explainable and reproducible.

📁 Files

BMW sales data (2010–2024).csv – Original dataset

AIassignmentdewesh.ipynb – Jupyter Notebook with complete feature engineering process

README.md – Project summary and documentation

🏁 Outcome

The final dataset is cleaned, encoded, scaled, and feature-engineered, making it fully ready for machine learning and analytical modeling.
Through proper handling of missing values, encoding, scaling, PCA, and feature selection, the data became more structured, interpretable, and suitable for predictive analysis.
