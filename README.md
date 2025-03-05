# Model and Predict Species Proportions

This repository contains an R Markdown tutorial for modeling and predicting tree species proportions using remote sensing data. The methodology combines **airborne laser scanning (ALS) and Sentinel-2 imagery**, toguether with **Random Forest modeling**, to predict species proportions at the stand level.

## Repository Contents

- `species_proportions_analysis.Rmd` – R Markdown file containing the full analysis pipeline.
- `README.md` – This file, providing an overview of the repository.

## Data description

The datasets used in this analysis should include:
- **Sample plot dataset** - Training data containing field-measured species proportions and remote sensing-derived predictors.
- **Validation plot dataset** - Independent dataset used to assess model performance.

## Methodology Overview

The analysis follows a **multi-step approach**:

1. **Load Data** – Sample plot and validation datasets are loaded.
2. **Prepare Data** – Remote sensing metrics are selected and cleaned for modeling.
3. **Train Random Forest Model** – A multi-response **Random Forest model** is trained to predict species proportions (Spruce, Pine, and Deciduous).
4. **Predict on Validation Data** – The trained model is applied to the validation dataset.
5. **Calibrate Predictions (Optional)** – A correction model is applied to adjust biases in the predictions.
6. **Normalize Predictions** – Predictions are normalized to ensure they sum to one.
7. **Aggregate at Stand Level** – Plot-level predictions are aggregated to stands.
8. **Evaluate Performance** – Error metrics such as RMSE and relative RMSE are calculated.
9. **Visualization** – Observed vs. predicted species proportions are plotted.

## Required Dependencies

Make sure to install the following R packages before running the analysis:

```r
install.packages(c("dplyr", "tidyr", "randomForestSRC", "data.table", "ggplot2"))
