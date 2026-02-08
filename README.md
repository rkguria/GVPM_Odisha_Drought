# Graph-based drought vulnerability propagation under climate change
## Coupling synchronization dynamics and population exposure in Odisha, India

This repository contains the **R scripts** used in the manuscript:

**Graph-based drought vulnerability propagation under climate change:  
Coupling synchronization dynamics and population exposure in Odisha, India**

**Authors:**  
Rajkumar Guria, Manoranjan Mishra*  
Department of Geography, Fakir Mohan University, Odisha, India  
*Corresponding author: Manoranjan Mishra (geo.manu05@gmail.com)

---

## 1. Overview

This study develops a **Graph-based Vulnerability Propagation Model (GVPM)** to quantify how meteorological drought impacts propagate spatially through synchronized drought networks and translate into population exposure under future climate change.

The workflow integrates:
- Bias-corrected CMIP6 rainfall projections  
- Nonparametric Standardized Precipitation Index (NSPI-6)  
- Event synchronization–based drought propagation networks  
- Population exposure (person-event) analysis  
- Graph-based vulnerability diffusion modelling  

This repository enables full inspection and reproduction of the **methodological and modelling framework** presented in the manuscript.

---

## 2. Data Availability and Description

### 2.1 Rainfall data
Processed, bias-corrected monthly CMIP6 rainfall data and derived multi-model ensemble (MME) rainfall for SSP2–4.5 and SSP5–8.5 scenarios are **archived on Zenodo**:

**https://doi.org/10.5281/zenodo.18523497**

The dataset includes:
- Bias-corrected monthly precipitation from five CMIP6 models  
  (MPI-ESM1-2-HR, BCC-CSM2-MR, INM-CM5-0, EC-Earth3, NorESM2-MM)
- Multi-model ensemble (MME) rainfall used for NSPI and GVPM analysis

Raw CMIP6 NetCDF outputs are publicly available from the **Earth System Grid Federation (ESGF)** and are not redistributed here due to data volume and redistribution policies.

---

### 2.2 Population data
Gridded population datasets derived from the **ISIMIP2b** protocol are also archived on Zenodo:

**https://doi.org/10.5281/zenodo.18523497**

These datasets include:
- Historical population (1981–2015)
- Future population projections (2025–2100) under SSP2 and SSP5  
- All population data are regridded to 0.25° spatial resolution to match rainfall data

---

## 3. Code Description

All scripts are written in **R** and organized to follow the methodological workflow of the manuscript.

Directory:


Directory:

Scripts should be executed sequentially:

1. `01_Bias_Correction_CMIP6.R` – Bias correction of CMIP6 rainfall using quantile mapping  
2. `02_CMIP6_Model_Evaluation.R` – Evaluation of CMIP6 rainfall against IMD observations  
3. `03_Bias_Correction_Comparison.R` – Comparison before and after bias correction  
4. `04_NSPI6_Calculation.R` – Historical NSPI-6 computation  
5. `05_Future_NSPI6_Calculation.R` – Future NSPI-6 computation under SSP scenarios  
6. `06_Event_Synchronization_Network.R` – Drought synchronization and network metrics  
7. `07_Population_Exposure.R` – Population exposure (person-event) analysis  
8. `08_Probability_Ratio_PR.R` – Probability ratio (PR) analysis  
9. `09_GVPM_Model.R` – Graph-based Vulnerability Propagation Model (GVPM)  
10. `10_GVPM_Sensitivity_Analysis.R` – Sensitivity and uncertainty analysis  

Each script includes a header specifying its purpose, input data, outputs, and the corresponding manuscript section.

---

## 4. Reproducibility

All figures and tables presented in the manuscript can be reproduced by:
1. Downloading the processed datasets from Zenodo  
   (https://doi.org/10.5281/zenodo.18523497)  
2. Running the scripts in the `R_code/` directory sequentially

---

## 5. Software Requirements

- R version ≥ 4.2  
- Key R packages:  
  `tidyverse`, `zoo`, `igraph`, `fitdistrplus`, `raster`, `sf`, `ncdf4`

---

## 6. License

All R scripts in this repository are released under the **MIT License**.  
The datasets archived on Zenodo are released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

---

## 7. Citation

### Dataset
Guria, R., & Mishra, M. (2026).  
*Processed rainfall and population datasets for graph-based drought vulnerability propagation analysis in Odisha, India* [Data set].  
Zenodo. https://doi.org/10.5281/zenodo.18523497

### Manuscript
If you use this code, please cite the associated manuscript:

Guria, R., & Mishra, M. (under review).  
*Graph-based drought vulnerability propagation under climate change:  
Coupling synchronization dynamics and population exposure in Odisha, India*.  
Environmental Modelling & Software.
