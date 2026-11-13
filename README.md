# AxelSMOTE: Axelrod-Guided Synthetic Oversampling for Imbalanced Learning

## 📌 Project Overview

Class imbalance is a common problem in machine learning where one class has significantly more samples than another. This often causes machine learning models to favour the majority class and perform poorly when identifying minority-class instances.

**AxelSMOTE** is a synthetic oversampling approach inspired by Axelrod's Cultural Dissemination Model. It aims to address class imbalance by generating synthetic minority-class samples through feature interactions, probabilistic feature exchange, and controlled noise injection.

Unlike traditional oversampling techniques that mainly rely on distance-based interpolation, AxelSMOTE introduces a structured approach to feature-level interaction while generating new samples.

## 🎯 Objectives

- Understand the challenges associated with imbalanced datasets.
- Study and implement the AxelSMOTE oversampling approach.
- Generate synthetic minority-class samples.
- Compare AxelSMOTE with conventional techniques such as SMOTE and Class Weighting.
- Evaluate the impact of oversampling on classification performance.
- Analyse the trade-off between classification performance and computational time.

## 🧠 About AxelSMOTE

AxelSMOTE draws inspiration from Axelrod's Cultural Dissemination Model, where agents interact and exchange traits based on their similarity.

The approach incorporates the following concepts:

1. **Feature Grouping and Trait Alignment:** Input features are organised into groups to represent structured feature relationships.

2. **Probabilistic Feature Exchange:** Feature values are exchanged between similar minority-class samples based on a similarity threshold.

3. **Gaussian Noise Injection:** A small amount of Gaussian noise is introduced during synthetic sample generation to improve variation and reduce repetitive patterns.

4. **Synthetic Sample Generation:** Newly generated samples are added to the minority class to reduce class imbalance.

## ⚙️ Methodology

The general workflow followed in the project is:

1. Load the selected imbalanced datasets.
2. Perform data preprocessing and identify minority and majority classes.
3. Apply the AxelSMOTE oversampling technique to generate synthetic minority samples.
4. Prepare balanced datasets using alternative approaches such as SMOTE and Class Weighting.
5. Train classification models on the resulting datasets.
6. Evaluate and compare the performance using suitable classification metrics.
7. Analyse the results across different experimental runs.

## 📊 Experimental Setup

The project explores the performance of different imbalance-handling approaches using the following classification algorithms:

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)

### Oversampling and Imbalance Handling Techniques

- AxelSMOTE (Proposed Approach)
- SMOTE
- Class Weighting

### Evaluation Metrics

The techniques are evaluated using:

- Minority Class Precision
- Minority Class Recall
- Minority Class F1-Score
- Precision-Recall AUC (PR-AUC)
- Execution Time

These metrics help assess classification performance, particularly the model's ability to identify minority-class instances.

## 📁 Repository Structure

```text
AxelSMOTE_ML/
│
├── AxelSMOTE_Master (1).ipynb
│   └── Main implementation and experiments
│
└── README.md
    └── Project documentation
```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/vranin/AxelSMOTE_ML.git
```

### 2. Navigate to the Project Directory

```bash
cd AxelSMOTE_ML
```

### 3. Open the Notebook

Open the notebook using Jupyter Notebook or Google Colab.

```bash
jupyter notebook
```

### 4. Execute the Notebook

Open `AxelSMOTE_Master (1).ipynb` and execute the cells sequentially to explore the implementation and experiments.

Install any required Python libraries mentioned in the notebook before execution.

## 🌍 Sustainable Development Goals (SDGs)

The project is associated with the following Sustainable Development Goals:

- **SDG 3 – Good Health and Well-being:** Improved minority-class identification can support machine learning applications in medical diagnosis.
- **SDG 8 – Decent Work and Economic Growth:** Better classification of software defects can contribute to improved software quality.
- **SDG 9 – Industry, Innovation and Infrastructure:** Explores innovative machine learning techniques for handling imbalanced datasets.

## 👩‍💻 Contributors

- **Tooba Siddeeqah**
- **Kashish Vallecha**

Department of Artificial Intelligence and Data Science  
Vivekanand Education Society's Institute of Technology (VESIT)

## 📚 References

- Axelrod, R. (1997). The Dissemination of Culture: A Model with Local Convergence and Global Polarization.
- AxelSMOTE: Axelrod-Guided Synthetic Oversampling for Imbalanced Learning.
- Chawla, N. V., et al. (2002). SMOTE: Synthetic Minority Over-sampling Technique. Journal of Artificial Intelligence Research.

## 📜 License

This repository is intended for academic and research purposes. Please refer to the original repository and associated research paper for attribution and usage conditions.
