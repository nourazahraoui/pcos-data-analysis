# Machine Learning Analysis of PCOS

##  Project Overview
This project presents a complete machine learning pipeline applied to the analysis of Polycystic Ovary Syndrome (PCOS) using clinical, hormonal, and lifestyle data. The objective is twofold: to build predictive models for PCOS classification and to analyze how different feature
representations influence model performance and interpretability.

The project combines data preprocessing, feature engineering,
dimensionality reduction, supervised learning, and unsupervised
clustering to provide both predictive and exploratory insights.

---

## Background
Polycystic Ovary Syndrome (PCOS) is a complex endocrine and metabolic
disorder characterized by symptoms such as anovulation, infertility,
obesity, insulin resistance, and polycystic ovaries. Multiple factors,
including lifestyle, genetics, and metabolic conditions, contribute to
its development.

This project applies data science and machine learning techniques to
better understand PCOS-related patterns and predictive indicators.

---

## Dataset
- **Source:** Publicly available PCOS clinical dataset  
- **Target variable:** PCOS (Yes / No)  
- **Features include:**
  - Hormonal measurements
  - Clinical and anthropometric indicators
  - Lifestyle and metabolic factors
  - Binary symptom indicators

Irrelevant identifiers (patient ID and file number) were removed during
initial exploration.

---

## Data Preprocessing
The preprocessing pipeline includes:
- Handling missing values (removal of a negligible number of incomplete rows)
- Binary encoding of categorical Yes/No variables
- Outlier detection and treatment using the IQR method (continuous variables only)
- Feature scaling using standardization (z-score normalization)
- Correlation-based feature selection to reduce redundancy

---

## Feature Engineering & Dimensionality Reduction
To address multicollinearity and improve model stability, dimensionality
reduction techniques were applied:

- **Principal Component Analysis (PCA):**
  - Retained approximately 80–90% of total variance
  - Improved performance for correlation-sensitive models

- **Factor Analysis (FA):**
  - Identified latent clinical factors
  - Revealed two dominant dimensions related to ovarian morphology and
    insulin resistance
  - Prioritized interpretability over pure predictive performance

---

## Machine Learning Models
Three supervised learning models were trained and evaluated across
different feature representations (original, PCA-based, and FA-based):

- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest

Model evaluation focused primarily on the **F1-score**, balancing
precision and recall.

---

## Cross-Validation & Model Selection
K-fold cross-validation was used to assess:
- Average predictive performance
- Stability and robustness across different data splits

This analysis emphasized that reliable model selection should consider
both performance and consistency.

---

##  Clustering Analysis
Unsupervised clustering was performed to explore hidden structures in
the data without using target labels:

- Applied on PCA and FA reduced feature spaces
- Optimal number of clusters determined using silhouette analysis
- Identified meaningful subgroups with distinct clinical and lifestyle
  profiles

Clustering provided complementary insights to supervised classification.

---

## Key Findings
- **SVM** achieved the best performance, particularly with PCA-transformed data
- **Random Forest** showed minimal benefit from dimensionality reduction
- **Logistic Regression** demonstrated stable and consistent performance
- PCA improved performance for models sensitive to correlated features
- FA enhanced interpretability by revealing latent clinical factors

---

## Limitations & Future Work
- Limited dataset size may affect generalization
- Linear feature selection and dimensionality reduction may not capture
  complex non-linear relationships

Future work could include:
- Non-linear dimensionality reduction techniques
- Advanced feature selection methods
- Integration of longitudinal or genetic data
- Evaluation on external datasets

---

##  Full Report
A detailed explanation of the methodology, experiments, and results is
available in the project report:

 **[PCOS Machine Learning Report (PDF)](PCOS report.pdf)**
 

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib / Seaborn
- Scikit-learn

---

##  Author
**Noura Zahraoui**  
Applied Computer Science student
