# GP3 Growth Curve Viewer

Version 1.0.0

An interactive R Shiny application for analysing microbial growth curve data generated from plate reader experiments.
🔗 **Live application:** https://raneemhi.shinyapps.io/gp3-growth-viewer/

---

## Overview

Growth Curve Viewer was developed for visualisation and quantitative analysis of microbial growth dynamics from high-throughput plate reader experiments.
The application enables rapid processing, filtering, and comparison of growth data across multiple strains, conditions, and antimicrobial treatments. Originally developed for experiments generated using the SProbotics Genomic Processor 3 (GP3) platform, the application is designed to support generic growth curve datasets from a wide range of experimental workflows and plate reader systems as its flexible structure allows the application to support multiple experimental designs and growth analysis workflows.

Potential applications include:

Antibiotic susceptibility and tolerance studies
Growth phenotype analysis
Functional genomics screening
High-throughput microbial phenotyping
Comparative strain analysis

---

## Functionality

The application includes:

Growth curve visualisation (replicate-level and mean ± SE)
Blank subtraction and OD normalisation
Experimental condition filtering
Outlier detection using IQR based methods
Area Under the Curve (AUC) analysis
Grouping by strain or user defined labels
Export of publication quality PDF figures


---

## Input data format

The application accepts standard plate reader growth datasets in .csv or .txt format alongside an experimental plate map in .xlsx format.

Plate reader input

Input files should contain:

- Plate identifiers
- Time or timestamp information
- Optical density (OD) measurements for each well

Plate map input

Plate map files should contain:

- Well identifiers
- Experimental conditions
- Replicate information
- Strain/sample names
- Optional concentration metadata
- Optional label mapping

Users may additionally upload a mapping table to group strains into:

- genes
- pathways
- phenotypic classes
- functional categories

---

## Outputs

The application generates:

- Replicate growth curves
- Mean growth curves with standard error
- OD distribution boxplots
- Outlier-filtered growth curves
- AUC summary plots
- Downloadable PDF reports

---

## Scientific context

This easy to use application was developed for wet-lab scientist to support quick analysis of bacterial growth dynamics generated using a plate reader platform. The tool enables reproducible processing and visualisation of plate reader data from high-throughput growth experiments, particularly under antibiotic exposure conditions.

Development and experimental design were conducted under the supervision of Dr. Danesh Moradigaravand.

## Affiliation

King Abdullah University of Science and Technology (KAUST)

Saudi Arabia

---

## Running locally

```r
install.packages(c(
  "shiny", "tidyverse", "lubridate",
  "readxl", "pracma", "stringr"
))

shiny::runApp()
```

---

## Deployment

This application is deployed using shinyapps.io.

---

## Citation

If you use this tool in your work, please cite:

Raneem Hirayban (2026). Growth Curve Viewer.
Available at: https://github.com/RaneemHi/gp3-growth-viewer

---

## Author

Raneem Hirayban
developed under the supervision of Dr. Danesh Moradigaravand.
