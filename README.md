# Epileptic Seizure Prediction Using Machine Learning

## Overview

This project investigates how preprocessing choices, model complexity, regularization strategies, and class imbalance handling affect generalization performance in epileptic seizure prediction tasks.

The study uses Logistic Regression as the baseline classifier and evaluates multiple preprocessing pipelines across three seizure-related datasets.

The project was completed as a Semester Major Assignment focusing on biomedical machine learning and EEG signal analysis.

---

## Objectives

This project aims to:

- Investigate the effect of preprocessing order on model performance
- Compare preprocessing pipelines
- Analyze overfitting and underfitting behavior
- Study regularization methods (L1, L2, Elastic Net)
- Evaluate sparsity effects
- Handle class imbalance using different strategies
- Compare generalization performance across datasets
- Analyze precision-recall tradeoffs

---

## Datasets

Three epileptic seizure datasets were used.

### Dataset 1

EEG seizure dataset with extracted statistical features.

Characteristics:

- Medium-sized dataset
- Binary classification
- Extracted EEG features

---

### Dataset 2

Large multi-class seizure prediction dataset.

Characteristics:

- Severe class imbalance
- Multi-class seizure categories
- High-dimensional extracted features

---

### Dataset 3

CHB-MIT EEG seizure dataset.

Characteristics:

- Raw EEG time-series signals
- Statistical feature extraction
- Small dataset size
- Strong overfitting tendency

---

## Preprocessing Pipelines

### Pipeline A

Normalization → Noise Removal → Feature Selection

Techniques:

- StandardScaler
- Variance Threshold
- SelectKBest

---

### Pipeline B

Feature Extraction → Scaling → PCA

Techniques:

- Statistical EEG feature extraction
- Standardization
- Principal Component Analysis (PCA)

---

## Baseline Model

Logistic Regression was used as the primary classifier.

Logistic regression equation:

\[
P(y=1|x)=\frac{1}{1+e^{-(\beta_0+\beta^Tx)}}
\]

Performance metrics:

- Accuracy
- F1-Score
- Precision
- Recall
- PR-AUC

---

## Overfitting and Underfitting Analysis

Intentional scenarios were created:

### Underfitting

- Strong regularization
- Limited model flexibility

### Overfitting

- Weak regularization
- High-dimensional feature space

Evaluations:

- Learning Curves
- Validation Curves
- Training vs Validation Accuracy

---

## Regularization Study

Three regularization approaches were compared:

### L1 Regularization (Lasso)

- Feature selection capability
- Sparse coefficients

### L2 Regularization (Ridge)

- Coefficient shrinkage
- Stable learning

### Elastic Net

Combination of:

- L1 penalty
- L2 penalty

Evaluated factors:

- Accuracy
- Stability
- Sparsity
- Generalization

---

## Class Imbalance Handling

Methods implemented:

### SMOTE Oversampling

Synthetic minority sample generation.

### Random Undersampling

Majority class reduction.

### Class Weighting

Balanced class contribution during optimization.

Evaluation criteria:

- Precision
- Recall
- F1-score
- Precision-Recall Tradeoff
- PR-AUC

---

## Project Structure

```text
project/

│
├── data/
│   ├── dataset1/
│   ├── dataset2/
│   └── dataset3/
│
├── notebooks/
│   └── seizure_prediction.ipynb
│
├── figures/
│   ├── learning_curves/
│   ├── pca_plots/
│   ├── sparsity_plots/
│   └── pr_auc/
│
├── report/
│   └── IEEE_Report.pdf
│
├── requirements.txt
│
├── README.md
│
└── src/
    ├── preprocessing.py
    ├── feature_extraction.py
    ├── modeling.py
    └── evaluation.py
```

---

## Installation

Clone repository:

```bash
git clone https://github.com/your-username/seizure-prediction.git

cd seizure-prediction
```

Create virtual environment:

```bash
python -m venv seizure_env
```

Activate environment:

Windows:

```bash
seizure_env\Scripts\activate
```

Linux/Mac:

```bash
source seizure_env/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Required Libraries

```txt
numpy
pandas
scikit-learn
matplotlib
seaborn
imbalanced-learn
pyarrow
scipy
jupyter
```

Install:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn imbalanced-learn pyarrow scipy jupyter
```

---

## Results Summary

Major findings:

- Preprocessing order significantly affects performance
- PCA improved feature stability
- Elastic Net provided balanced sparsity and stability
- Dataset imbalance strongly influenced recall
- SMOTE improved minority class detection
- Dataset 3 demonstrated strongest overfitting tendency

---

## Comparative Analysis

Research questions addressed:

✔ Does preprocessing order affect results?

✔ Which regularization generalizes best?

✔ Does Elastic Net outperform L1/L2?

✔ How does imbalance handling interact with regularization?

---

## Future Work

Potential improvements:

- Deep learning architectures
- CNN-based EEG classification
- Transformer-based seizure prediction
- Real-time EEG analysis
- Hybrid feature engineering

---

## Author

**Hafiz Ullah**

Assistant Professor of Mathematics

Abasyn University Peshawar

Pakistan

---

## License

This project is developed for academic and educational purposes.

---

## Citation

If using this work:

```

Hafiz Ullah,
"Investigating Preprocessing Choices, Model Complexity, and Regularization Strategies in Epileptic Seizure Prediction",
Semester Major Assignment,
2026.

```
