# Single-Cell RNA-seq Analysis with Machine Learning

End-to-end analysis of single-cell RNA sequencing (scRNA-seq) data, combining unsupervised learning, biological interpretation, and supervised machine learning.

---

## Overview

This project demonstrates how high-dimensional gene expression data can be transformed into:

- biologically meaningful cell populations  
- a predictive machine learning model  

The workflow integrates clustering, marker-gene analysis, and classification to bridge bioinformatics and machine learning.

---

## Key Results

- Identified major immune cell types:
  - T cells, B cells, monocytes, NK cells, dendritic cells  
- Achieved **~97–98% classification accuracy** using PCA features  
- Demonstrated that:
  - cell types are **linearly separable in PCA space**
  - model decisions align with **known biological markers**

---

## Methodology

### 1. Preprocessing
- Quality control using gene counts and mitochondrial percentage  
- Normalization and log transformation  

### 2. Feature Engineering
- Selection of 2,000 highly variable genes  
- PCA (dimensionality reduction to 50 components)  

### 3. Unsupervised Learning
- KNN graph construction  
- Leiden clustering  
- UMAP visualization  

### 4. Biological Interpretation
- Differential expression analysis (Wilcoxon test)  
- Marker-gene-based cell-type annotation  

### 5. Supervised Learning
- Models: Random Forest, Logistic Regression, XGBoost  
- Input: PCA features  
- Output: cell-type prediction  

---

## Model Performance

| Model | Accuracy |
|------|--------|
| Logistic Regression | ~98% |
| Random Forest | ~97% |
| XGBoost | ~98% |

- Minor confusion observed between closely related cell types (e.g., monocyte subtypes)
- Performance on rare classes limited by sample size

---

## Feature Importance (Interpretability)

Model importance was mapped back to gene space via PCA loadings.

Top genes included:

- Cytotoxic markers: `NKG7`, `GZMB`, `PRF1`, `GNLY`  
- Monocyte markers: `FCGR3A`, `TYROBP`  
- Antigen presentation: `HLA-DPA1`  

This confirms that the model relies on biologically meaningful signals.

---

## Key Insights

- PCA effectively captures biological structure in scRNA-seq data  
- Cell types are largely separable with simple models  
- Combining clustering + ML creates a powerful analysis pipeline  
- Feature importance can be linked back to gene-level biology  

---

## Tools

- Python  
- Scanpy  
- Scikit-learn  
- XGBoost  
- NumPy / Pandas
- Matplotlib
- Google Colab

---

## Future Work

- External dataset validation  
- Multi-omics integration  
- Deep learning approaches  

---

## Author

Johra Muhammad Moosa  
PhD, Computer Sceince (Bioinformatics)  
Machine Learning | Computational Biology

