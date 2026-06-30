# 311 Spatial Analytics Pipeline

A reproducible spatial analytics pipeline for investigating neighborhood health determinants using municipal 311 service requests and Small Area Estimation (SAE).

This project was presented at **AAG 2024** as

**[A Civic Stethoscope for Healthy City: Utilizing 311 Requests to Monitor Neighborhood Health Determinants](https://drive.google.com/file/d/14ieHtIqg9TCMkLTe5ZJqOWUIEkAvD9n4/view?usp=drive_link)**

---

# Project Overview

Municipal 311 service requests provide high-resolution records of neighborhood conditions, including illegal dumping, abandoned vehicles, street maintenance, sewer problems, traffic signals, tree maintenance, and other non-emergency public service requests.

Rather than treating these reports as isolated service events, this project investigates whether 311 requests can serve as neighborhood-level indicators of urban health determinants.

The repository implements a complete spatial analytics pipeline that integrates Small Area Estimation, spatial feature engineering, dimensionality reduction, spatial econometric modeling, and hotspot analysis.

---

# Figures

## Principal Component Analysis of 311 Request Patterns

<img src="figures/Figure2_311PC.jpg" width="800" alt="PCA results of 311 request patterns">

## Spatial Clustering of 311 Requests

<img src="figures/Figure3_311Cluster.jpg" width="800" alt="Spatial clustering results of 311 requests">

## Hotspot Analysis

<img src="figures/Hotspot_5000_(CBG)_4@1000x-100.jpg" width="800" alt="Hotspot analysis of 311 requests">

# Pipeline Overview

```text
                    SMART BRFSS Survey
                            │
                            ▼
                Python Data Preparation
                            │
                            ▼
                  GLMM (glmmTMB)
                            │
                            ▼
      Multilevel Regression with Poststratification
                      (Small Area Estimation)
                            │
                            ▼
       Neighborhood Mental Health Estimates
                            │
                            ▼
            311 Data Preprocessing (Python)
                            │
                            ▼
        PCA + K-means Feature Extraction
                            │
                            ▼
           OLS + Moran's I Analysis
                            │
                            ▼
     Spatial Model Selection (SLM / SEM / SDM)
                            │
                            ▼
          Hotspot Analysis & Validation
```

---

# Methodology

## Small Area Estimation (SAE)

Neighborhood-level mental health prevalence was estimated using **Multilevel Regression with Poststratification (MRP)**.

The workflow consisted of three stages:

1. Fit a Generalized Linear Mixed Model (GLMM) using **glmmTMB**.

2. Predict mental health prevalence across demographic groups while accounting for hierarchical geographic variation.

3. Apply poststratification using Census population distributions to estimate neighborhood-level prevalence.

These estimates served as the neighborhood-level outcome variables for the subsequent spatial analyses.

---

## Spatial Analytics

The estimated mental health prevalence was linked with municipal 311 service request records through a reproducible spatial analytics workflow.

Major analytical components include:

- Data preprocessing
- Spatial feature engineering
- Principal Component Analysis (PCA)
- K-means clustering
- Ordinary Least Squares (OLS)
- Moran's I spatial autocorrelation
- Spatial Lag Model (SLM)
- Spatial Error Model (SEM)
- Spatial Durbin Model (SDM)
- Getis-Ord Gi* hotspot analysis
- Confusion matrix validation

---

# Technology Stack

### Programming

- Python
- R

### Statistical Modeling

- GLMM (glmmTMB)
- Multilevel Regression with Poststratification (MRP)

### Spatial Analysis

- Principal Component Analysis (PCA)
- K-means Clustering
- Moran's I
- Spatial Econometric Models
- Getis-Ord Gi*

### GIS

- ArcGIS Pro

---

# Repository Structure

```text
311-spatial-analytics/

├── code/
│   ├── 1_DataPreprocessing_for_MLR.ipynb
│   ├── 2_data_for_prediction.ipynb
│   ├── 3_fit_model_Rmarkdown.Rmd
│   ├── 4_data_for_calculating_prevalence.ipynb
│   ├── 5.1_311_data_preprocessing.ipynb
│   ├── 5.2_OLS_data_preparation.ipynb
│   ├── 6.1_OLS+Moran'sI.Rmd
│   └── 6.2_spatial_model_selection.Rmd
│
├── data/
│   ├── Raw datasets
│   └── Processed datasets
│
├── output/
│   ├── Model outputs
│   ├── Statistical summaries
│   └── Validation results
│
├── figures/
│   ├── Tables used in manuscript
│   ├── Maps
│   ├── Figures
│   ├── Adobe Illustrator files
│   └── Visualizations
│
└── README.md
```

---

# Project Highlights

- Built an end-to-end spatial analytics pipeline combining Python, R, and GIS workflows.
- Estimated neighborhood-level mental health prevalence using Small Area Estimation (MRP).
- Engineered spatial indicators from large-scale municipal 311 service request records.
- Compared multiple spatial econometric models to quantify neighborhood-level spatial relationships.
- Presented the project at the **American Association of Geographers (AAG) Annual Meeting 2024**.

---
