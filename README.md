# 311 Service Request Spatial Analytics Pipeline

This repository documents an R-based spatial analytics project that uses 311 service request data to study neighborhood-level urban health determinants in Oakland, California.

The project was presented at AAG 2024 as **"A Civic Stethoscope for Healthy City: Utilizing 311 Requests to Monitor Neighborhood Health Determinants."**

## Project Overview

311 service requests provide high-resolution records of local urban conditions, including issues such as illegal dumping, street maintenance, sewer problems, traffic signals, trees, and other non-emergency municipal concerns.

This project explores whether these records can serve as neighborhood-scale indicators of urban well-being and mental health-related spatial patterns.

## Research Workflow

The analysis follows four main steps:

1. Preprocess Oakland 311 service request records and aggregate request categories to neighborhood spatial units.
2. Use PCA and K-means clustering to identify major reporting patterns and neighborhood profiles.
3. Test spatial associations between 311 request categories and mental health estimates using OLS and Moran's I.
4. Build spatial regression models, including SLM, SEM, and SDM, and evaluate hotspot prediction using Getis-Ord Gi*.

## Methods

- Principal Component Analysis (PCA)
- K-means clustering
- Ordinary Least Squares (OLS)
- Moran's I spatial autocorrelation test
- Spatial Lag Model (SLM)
- Spatial Error Model (SEM)
- Spatial Durbin Model (SDM)
- Getis-Ord Gi* hotspot analysis
- Confusion matrix evaluation for hotspot and coldspot prediction

## Tools

- R
- R spatial/statistical packages
- ArcGIS Pro for map preparation and visualization

## Presentation

This work was presented at the **American Association of Geographers Annual Meeting 2024** in Honolulu, Hawaiʻi.

## Repository Purpose

This repository is intended to organize the research workflow, code structure, and project documentation for the 311 spatial analytics project. It highlights how public municipal service records can be transformed into spatial indicators for neighborhood-level analysis.
