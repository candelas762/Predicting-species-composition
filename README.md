# Predicting-species-composition
Model and Predict Species Proportions

This repository contains an R Markdown tutorial for modeling and predicting tree species proportions using remote sensing data. The methodology leverages airborne laser scanning (ALS) and Sentinel-2 imagery, combined with Random Forest regression, to estimate species proportions at the stand level.

Repository Contents

species_proportions_analysis.Rmd – R Markdown file containing the full analysis pipeline.

data/ – Folder containing training and validation datasets.

README.md – This file, providing an overview of the repository.

Methodology Overview

The analysis follows a multi-step approach:

Load Data – Sample plot and validation datasets are loaded.

Prepare Data – Remote sensing metrics are selected and cleaned for modeling.

Train Random Forest Model – A multi-response Random Forest model is trained to predict species proportions (Spruce, Pine, and Deciduous).

Predict on Validation Data – The trained model is applied to the validation dataset.

Calibrate Predictions (Optional) – A correction model is applied to adjust biases in the predictions.

Normalize Predictions – Predictions are normalized to ensure they sum to one.

Aggregate at Stand Level – Plot-level predictions are aggregated to stands.

Evaluate Performance – Error metrics such as RMSE and relative RMSE are calculated.

Visualization – Observed vs. predicted species proportions are plotted.

Required Dependencies

Make sure to install the following R packages before running the analysis:

install.packages(c("dplyr", "tidyr", "randomForestSRC", "data.table", "ggplot2"))

How to Use

# Clone this repository
git clone https://github.com/yourusername/species_proportions_analysis.git

# Navigate to the repository
cd species_proportions_analysis

# Open the R Markdown file in RStudio or another R environment
# Run the code chunks step by step or knit the document to generate a full report

Data Description

The datasets used in this analysis include:

Sample Plot Dataset (data/sample_plot_dataset.csv) – Training data containing field-measured species proportions and remote sensing-derived predictors.

Validation Plot Dataset (data/validation_plot_dataset.csv) – Independent dataset used to assess model performance.

Citation

If you use this repository or methodology, please cite:

@article{CandelasBielza2024,
  author = {Candelas Bielza, J. and others},
  title = {Predicting tree species composition using airborne laser scanning and multispectral data in boreal forests},
  journal = {Science of Remote Sensing},
  year = {2024},
  volume = {100154}
}

License

This project is licensed under the MIT License - see the LICENSE file for details.

Maintainer: Jaime Candelas BielzaDate: March 1, 2025

