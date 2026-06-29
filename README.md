# 311 Spatial Analytics Pipeline

A reproducible geospatial analytics pipeline for transforming large-scale 311 service request records into neighborhood-level spatial features for urban pattern discovery and spatial modeling.

This project integrates municipal service requests, census demographics, and public health datasets to automate spatial data processing, feature engineering, hotspot detection, and spatial statistical modeling.

---

## Motivation

311 service requests provide high-resolution observations of urban conditions. This project explores how large-scale geospatial data can be transformed into analytical features that support neighborhood-level spatial analysis and decision making.

---

## Key Features

* Automated preprocessing of multi-year 311 service request datasets
* Spatial aggregation from point observations to census block groups
* Feature engineering for neighborhood-level spatial indicators
* Hotspot detection using Getis-Ord Gi*
* Spatial autocorrelation analysis using Moran's I
* Spatial regression including OLS, SLM, SEM, and SDM
* Interactive visualization using ArcGIS StoryMap

---

## Technical Stack

**Programming**

* Python
* R
* SQL

**GIS**

* ArcGIS Pro
* GeoPandas
* ArcPy

**Spatial Analysis**

* PySAL
* Moran's I
* Hotspot Analysis
* Spatial Regression

**Visualization**

* ArcGIS StoryMap
* Matplotlib

---

## Workflow

```
311 Requests
        │
        ▼
Data Cleaning
        │
        ▼
Spatial Aggregation
        │
        ▼
Feature Engineering
        │
        ▼
Spatial Statistics
        │
        ▼
Spatial Regression
        │
        ▼
Hotspot Detection
        │
        ▼
Visualization
```

---

## Repository Structure

```
src/
data/
outputs/
docs/
```

---

## Results

* Processed over 2 million geospatial records
* Generated neighborhood-level spatial indicators
* Identified significant spatial clusters using Moran's I and Getis-Ord Gi*
* Developed spatial regression models to quantify relationships between 311 requests and neighborhood mental health

---

## Future Work

* Deploy as an interactive WebGIS application
* Support real-time municipal data ingestion
* Incorporate graph-based spatial learning methods
* Extend to multi-city spatial analytics
