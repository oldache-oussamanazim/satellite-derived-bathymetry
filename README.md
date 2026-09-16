Satellite-Derived Bathymetry Using Sentinel-2

Overview

This project investigates the use of Sentinel-2 multispectral imagery for estimating shallow-water bathymetry.

The study combines field bathymetric measurements, satellite-derived spectral information, empirical bathymetric methods and machine learning to evaluate the potential of Satellite-Derived Bathymetry (SDB) for shallow coastal environments.

Objectives

- Extract Sentinel-2 spectral and derived features related to water depth.
- Evaluate empirical bathymetric approaches.
- Develop a Random Forest bathymetric model.
- Compare model performance using quantitative validation metrics.
- Investigate the importance of spatial validation for bathymetric modelling.
- Produce a spatial bathymetry map for the study area.

Data

The analysis uses:

- Sentinel-2 multispectral imagery
- Field bathymetric measurements
- Spectral bands and derived indices
- Spatially derived predictors

The study focuses on shallow coastal waters where satellite-derived bathymetry can potentially support preliminary coastal and marine applications.

Methods

1. Sentinel-2 Feature Extraction

The satellite imagery is processed to derive predictors including:

- B2 — Blue
- B3 — Green
- B4 — Red
- B8 — Near Infrared
- NDWI
- MNDWI
- Texture features
- Stumpf ratio

2. Empirical Bathymetric Models

Two empirical approaches are evaluated:

- Stumpf ratio transform
- Lyzenga logarithmic transform

3. Random Forest

A Random Forest regression model is used to investigate the relationship between Sentinel-2-derived predictors and measured water depth.

Model development includes:

- Feature selection
- Training/testing
- Hyperparameter comparison
- Spatial validation
- Performance assessment

Validation

Model performance is evaluated using:

- R²
- RMSE
- MAE
- Bias

Both conventional random validation and spatial validation are considered in order to investigate the effect of spatial dependence between training and validation observations.

Results

Random Forest Bathymetry

The resulting Random Forest bathymetry map is shown below.

"Random Forest Bathymetry" (results/figures/rf_bathymetry_map.png)

Further quantitative results and validation figures will be added as the analysis is finalized.

Workflow

Sentinel-2 imagery
        ↓
Pre-processing
        ↓
Spectral & derived features
        ↓
Field bathymetric data
        ↓
Feature extraction
        ↓
 ┌───────────────┬───────────────┐
 │               │               │
Stumpf         Lyzenga       Random Forest
 │               │               │
 └───────────────┴───────────────┘
                 ↓
          Spatial validation
                 ↓
        Model performance
                 ↓
        Bathymetry mapping

Tools

- Google Earth Engine
- Python
- Sentinel-2
- GIS
- ESA SNAP
- Random Forest

Project Status

In progress

The repository is being progressively updated with scripts, validation results, figures and methodological documentation.
