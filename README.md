# Unsupervised Patient Phenotyping for Stroke Risk

Testing Intruction

Install dependencies ```pip install -r requirements.txt```
Run CMD: ```jupyter notebook stroke_lab_analysis.ipynb```

### Background

Stroke is one of the leading cause of death and long-term disability worldwide. It affects millions of people annually. While there is substantial research focused on predicting stroke occurrence using supervised machine learning, there is less published analysis on understanding the natural heterogeneity in patient populations before outcomes occur. Clinical practice often treats risk factors like age, hypertension, diabetes, lifestyle behaviors as independent predictors. But patients rarely present with isolated risk factors, more often they arrive with complex, interrelated profiles.

### Problem Statement

Using unsupervised learning reveal patient grouping without imposing stroke outcomes as a training signal. Can unsupervised learning can be used to discover meaningful patient phenotypes based on demographics, clinical, and lifestyle characteristics? And if meaningful patient phenotypes are defined do they align with different stroke risks?

### Project Objectives

Healthcare Stroke Prediction Dataset (5,110 patients)

1. Identify latent patient subtypes through unsupervised clustering (K-Means, Gaussian Mixture Models, Hierarchical Clustering)

2. Characterize each phenotype by demographic, clinical, and lifestyle features

3. Compare clustering algorithms using multiple internal validation metrics (Silhouette Score, Davies-Bouldin Index, Calinski-Harabasz Index)

4. Apply dimensionality reduction (PCA, t-SNE) to understand feature space structure and visualize clusters

5. Perform post-hoc analysis examining stroke prevalence within discovered clusters (without using stroke labels during clustering)

6. Compare with supervised learning to demonstrate the unique value of unsupervised phenotyping for data efficiency and interpretability

### Methods

Phase 1: Exploratory Data Analysis (EDA) with statistical validation

Phase 2: Data preprocessing (missing value imputation, encoding, scaling)

Phase 3: Dimensionality reduction and feature interpretation

Phase 4: Multi-algorithm clustering with hyperparameter optimization

Phase 5: Cluster validation and clinical interpretation

Phase 6: Comparison with supervised baselines

### Final Results Summary

Discovered hidden patient groups in stroke data using unsupervised machine learning—without looking at stroke outcomes. Found an elderly high-risk cluster with 8.03% stroke rate (1.64× population average).

| Cluster | n (%)        | Description             | Age  | Stroke Rate | vs Baseline |
|---------|--------------|-------------------------|------|-------------|-------------|
| 0       | 688 (13.5%)  | Children                | 7 yrs  | 0.29%       | 0.06×       |
| 1       | 822 (16.1%)  | Elderly High-Risk       | 60 yrs | 8.03%       | 1.64×    |
| 2       | 3,577 (70.0%)| Working Adults          | 47 yrs | 5.06%       | 1.04×       |
| 3       | 22 (0.4%)    | Special Cases           | 16 yrs | 0.00%       | 0.00×       |


Cluster 1 Profile: 99.6% self-employed, 18% hypertension, 10% heart disease, BMI 30.1, glucose 113 mg/dL

Source: Kaggle Stroke Prediction Dataset
Link: https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset
