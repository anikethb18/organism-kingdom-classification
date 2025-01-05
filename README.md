# Organism-kingdom-classification
Machine learning pipeline for classifying organisms based on DNA codon usage patterns.
# Organism Prediction Based on Codon Usage

## Overview
This project utilizes codon usage patterns to predict the organism's kingdom through machine learning models. By analyzing the frequency of codons in DNA sequences, the project achieves high accuracy in biological classification tasks. The top-performing model, K-Nearest Neighbors (KNN), achieves an accuracy of 97%.

---

## Features
- Classification of organisms into kingdoms based on codon frequency patterns.
- Preprocessing techniques like outlier removal, encoding, and normalization.
- Implementation of multiple machine learning models: KNN, Logistic Regression, Random Forest, and SVM.
- Feature selection and hyperparameter tuning for performance optimization.

---

## Dataset
- **Source**: [UCI Codon Usage Dataset](https://archive.ics.uci.edu/dataset/577/codon+usage)
- **Description**:
  - **Instances**: 13,028
  - **Features**: 69 (including codon frequencies and metadata)
  - **Target Variable**: Kingdom of the organism (e.g., archaea, bacteria, virus, etc.)
- **Preprocessing**:
  - Outlier detection and removal using IQR, reducing the dataset to 3,744 rows.
  - Encoding categorical variables and normalizing numerical features.

---

## Methodology
### Preprocessing
- Outlier removal.
- Encoding categorical variables.
- Normalization of codon frequency data.

### Models
1. **K-Nearest Neighbors (KNN)**:
   - Tuned with `n_neighbors=6`.
   - Accuracy: 97%.
2. **Logistic Regression**:
   - Multi-class One-vs-Rest approach.
   - Accuracy: 76%.
3. **Random Forest**:
   - Decision tree-based ensemble method.
   - Accuracy: 90%.
4. **Support Vector Machines (SVM)**:
   - Linear Kernel: 62% accuracy.
   - Non-linear Kernel: 91% accuracy.

### Feature Selection
- Correlation analysis to reduce multicollinearity.
- Wrapper-based feature selection using bi-directional elimination.

---

## Results
| Model              | Accuracy | Precision | Recall | F1 Score |
|--------------------|----------|-----------|--------|----------|
| **KNN**            | 97%      | 96%       | 97%    | 97%      |
| Logistic Regression| 76%      | 75%       | 76%    | 75%      |
| Random Forest      | 90%      | 90%       | 90%    | 89%      |
| SVM (Non-linear)   | 91%      | 91%       | 91%    | 91%      |

### Visualizations
- Confusion matrices for each model.
- Correlation heatmap of features.
- Classification reports for precision, recall, and F1 score.

---

## Future Enhancements
- Incorporate ensemble approaches combining top-performing models.
- Extend feature engineering with domain expert insights.
- Explore advanced algorithms like XGBoost and Extreme Learning Machines.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/username/organism-prediction.git
