# Day-12
Data Transformation in Machine Learning

Objective

To understand and implement various data transformation techniques used in machine learning for preparing raw data before model training.

Introduction

Data transformation is the process of converting raw data into a suitable format for analysis and machine learning. Real-world data often contains missing values, outliers, categorical variables, and inconsistent formats. Data transformation helps improve data quality and model performance.

Techniques Used

1. Handling Missing Data

Missing values can negatively affect model performance. Common methods include:

- Removing missing values
- Mean, Median, and Mode Imputation
- KNN Imputation
- Forward Fill and Backward Fill
- Interpolation

2. Handling Outliers

Outliers are extreme values that differ significantly from other observations.
Methods:

- Z-Score
- IQR Method
- Box Plot Analysis
- Log Transformation
- Truncation

3. Normalization and Standardization

Normalization
Scales data between 0 and 1.

Formula:
x' = (x - min(X)) / (max(X) - min(X))

Standardization
Transforms data so that mean = 0 and standard deviation = 1.

Formula:
x' = (x - mean(X)) / std(X)

4. Encoding Categorical Variables

Methods:

- One-Hot Encoding
- Label Encoding
- Ordinal Encoding

5. Handling Skewed Data

Methods:

- Log Transformation
- Square Root Transformation
- Box-Cox Transformation
- Yeo-Johnson Transformation
- Quantile Transformation

6. Feature Engineering

Creating new features from existing features to improve model performance.
Examples:

- Polynomial Features
- Interaction Terms
- Domain-Specific Features

7. Dimensionality Reduction

Methods:

- Principal Component Analysis (PCA)
- t-SNE

8. Text Data Transformation

Methods:

- Text Cleaning
- Tokenization
- Stopword Removal
- Stemming
- Lemmatization
- TF-IDF
- Word Embeddings

Advantages

- Improves model accuracy
- Handles missing values effectively
- Faster model convergence
- Reduces dimensionality
- Enhances feature quality

Disadvantages

- Information loss if applied incorrectly
- Risk of overfitting
- Data leakage
- Increased preprocessing complexity

Conclusion

Data transformation is an essential step in machine learning. Proper transformation techniques improve data quality, enhance model performance, and help build reliable predictive models.
