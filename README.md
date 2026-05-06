# GP3 Growth Curve Viewer

An interactive **R Shiny application** for analysing bacterial growth curves from plate reader experiments.

🔗 **Live application:** https://raneemhi.shinyapps.io/gp3-growth-viewer/

---

## 🧬 Functionality

GP3 Growth Curve Viewer was developed to analyse plate reader growth data and extract key quantitative metrics, including:

* Growth curve visualisation (replicate-level and mean ± SE)
* Blank subtraction and OD normalisation
* Condition and concentration filtering
* Outlier detection using IQR-based methods
* Area Under the Curve (AUC) calculation
* Grouping by strain or user-defined gene/functional labels
* Export of publication-quality figures (PDF)

---

## 🧪 Experimental platform

Data analysed with this tool are generated using the **SandPRobotics Genomic Processor 3 (GP3)**, an automated platform for high-throughput microbial growth experiments and phenotypic screening.

---

## 🧪 Input requirements

### Plate reader output

* Format: `.csv` or `.txt`
* Must include:

  * Plate identifier
  * Timestamp columns
  * Optical density (OD) measurements

### Plate map file

* Format: `.xlsx`
* Required columns:

  * wells
  * Row
  * Column
  * Condition
  * Concentration (ug/ml)
  * Replicates
  * Strain

### Optional label mapping file

* Format: `.xlsx`
* Columns:

  * Strain
  * Label (e.g. gene, pathway, phenotype group)

---

## ⚙️ Analysis workflow

1. Upload plate reader output and plate map
2. (Optional) Upload strain-to-label mapping file
3. Define blank wells and experimental conditions
4. Generate growth curves and summary statistics
5. Apply outlier filtering if required
6. Visualise AUC and export results

---

## 📊 Outputs

The application generates:

* Replicate growth curves
* Mean growth curves with standard error
* OD distribution boxplots
* Outlier-filtered growth curves
* AUC summary plots (mean ± SE)
* Downloadable PDF reports

---

## 🧠 Scientific context

This easy to use application was developed for wet-lab scientist to support quick analysis of bacterial growth dynamics generated using the SandPRobotics Genomic Processor 3 (GP3) platform. The tool enables reproducible processing and visualisation of plate reader data from high-throughput growth experiments, particularly under antibiotic exposure conditions.

Development and experimental design were conducted under the supervision of Dr. Danesh Moradigaravand.

---

## ▶️ Running locally

```r
install.packages(c(
  "shiny", "tidyverse", "lubridate",
  "readxl", "pracma", "stringr"
))

shiny::runApp()
```

---

## 🌐 Deployment

This application is deployed using shinyapps.io.

---

## 📄 Citation

If you use this tool in your work, please cite:

Hirayban, R. *GP3 Growth Curve Viewer* (2026).

---

## 👩🏾‍🔬 Author

Raneem Hirayban
developed as part of research conducted under the supervision of Dr. Danesh Moradigaravand.
