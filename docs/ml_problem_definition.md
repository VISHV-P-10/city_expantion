# ML Problem Definition

## Problem Statement
Given multi-temporal satellite imagery and relevant
geospatial variables, identify areas of urban expansion
and develop a model that estimates the spatial probability
of future urban growth.

## Input

## Output
Output A — Detection
Urban change map

For example:

0 = no new urban growth
1 = newly developed area
Output B — Prediction
Urban growth probability map

## Features
 candidate features
 ->
Spectral bands
NDVI
NDBI
NDWI
Distance from existing built-up area
Distance from roads
Distance from water
Slope
Elevation
Land-use information
## Target
Target = whether a location experienced urban expansion
during the selected future time interval.
or 
0 → no observed urban growth
1 → observed urban growth

## Evaluation Metrics
We will evaluate both pixel-level predictive performance
and spatial agreement between predicted and observed growth.

## Baseline
1. NDBI threshold-based built-up detection
2. Logistic Regression
Random Forest


## Assumptions
- Satellite observations are sufficiently comparable across
  the selected time periods.

- The selected study area has sufficient historical imagery.

- Candidate growth-driver variables can be spatially aligned.

- Observed historical urban expansion can be used as a target
  for supervised learning.

## Potential Challenges
- Cloud contamination
- Seasonal differences
- Different image acquisition conditions
- Mixed pixels
- Confusion between built-up land and bare soil
- Spatial resolution limitations
- Class imbalance
- Spatial leakage
- Temporal leakage
- Limited ground truth
- Misalignment between datasets