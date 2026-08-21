# Evaluation of Carbon Sink and Sequestration Potential of Trees within Hall-8

### Field-Based Biomass Estimation and Age-Based Growth Projection

A field-based assessment of tree biomass, carbon stock, and estimated annual CO₂ sequestration potential of trees within Hall-8, Indian Institute of Technology Kanpur.

---

## Overview

Trees act as important terrestrial carbon sinks by absorbing atmospheric carbon dioxide (CO₂) and storing carbon in their biomass.

This project evaluates the existing carbon stock and estimated carbon sequestration potential of trees located within **Hall-8, IIT Kanpur**. The analysis is based on a primary field survey of trees, using measurements of:

* Tree species
* Circumference
* Tree height
* Wood density
* Age information for a subset of trees

These field measurements were used to estimate:

1. Diameter at Breast Height (DBH)
2. Above-Ground Biomass (AGB)
3. Below-Ground Biomass (BGB)
4. Total tree biomass
5. Current carbon stock
6. Stored CO₂-equivalent
7. Subsequent-year biomass using an age-based growth model
8. Estimated annual carbon sequestration potential

A **Chave et al. (2014) allometric model** was used for above-ground biomass estimation, while a **Chapman–Richards growth function** was used to model the relationship between tree age and circumference and to project subsequent-year growth.

The study surveyed **228 trees belonging to 19 species** within the Hall-8 study area.

---

## Project Objectives

The main objectives of the study are:

* To prepare an inventory of trees present within Hall-8.
* To estimate the above-ground biomass (AGB) of the surveyed trees.
* To estimate below-ground biomass (BGB).
* To estimate the amount of carbon currently stored in the tree biomass.
* To convert stored carbon into CO₂-equivalent terms.
* To estimate tree age using an age–circumference growth relationship.
* To project subsequent-year circumference and biomass.
* To estimate annual carbon sequestration potential from the projected increase in biomass.
* To identify tree species contributing most strongly to the carbon sink.

---

## Research Question

The central question addressed by this project is:

> **How much carbon is currently stored in the trees within Hall-8, IIT Kanpur, and what is their estimated potential for additional CO₂ sequestration through future tree growth?**

The analysis also investigates:

> **Which tree species contribute most strongly to the existing carbon stock and estimated annual sequestration potential?**

---

## Study Area

**Location:** Hall-8, Indian Institute of Technology Kanpur

The field inventory covered trees distributed across different locations surrounding Hall-8, including blocks and adjoining areas such as:

* Block A–B
* Block B–C
* Block C–D
* Block D–Mess
* Block E–Mess
* Block F–E
* Block H–G
* Hall Office–Block H
* Mess Front
* Outer Road

The inventory recorded a total of **228 trees** across **19 species**.

---

# Dataset

## Primary Field Data

The project uses primary tree inventory data collected within Hall-8.

The field measurements include information required for biomass and carbon estimation, particularly:

| Variable      | Description                                                      |
| ------------- | ---------------------------------------------------------------- |
| Species       | Scientific name of the tree species                              |
| Circumference | Tree circumference measured at approximately 1.37 m above ground |
| Height        | Total tree height                                                |
| Wood density  | Species-specific wood density                                    |
| Age           | Age information available for a subset of trees                  |

## Circumference was measured at approximately **1.37 metres above ground level**, following the standard convention used for forest inventory. Trees with circumference below **8 cm** were excluded from the analysis.

## Tree Inventory

The field survey identified:

| Indicator                      |  Value |
| ------------------------------ | -----: |
| Total trees                    |    228 |
| Number of species              |     19 |
| Measurement height             | 1.37 m |
| Minimum circumference included |   8 cm |

The most abundant species was **Polyalthia longifolia**, with 102 trees, followed by **Azadirachta indica** with 32 trees and **Mangifera indica** with 21 trees.

---

# Methodology

The analysis follows the sequence:

```text
Field Measurements
       │
       ├── Species
       ├── Circumference
       └── Height
       │
       ▼
Diameter at Breast Height (DBH)
       │
       ▼
Above-Ground Biomass (AGB)
       │
       ▼
Below-Ground Biomass (BGB)
       │
       ▼
Total Biomass
       │
       ▼
Carbon Stock
       │
       ▼
CO₂ Equivalent
```

For future growth estimation, the workflow is extended as:

```text
Age–Circumference Data
        │
        ▼
Chapman–Richards Growth Model
        │
        ▼
Estimated Tree Age
        │
        ▼
Annual Circumference Growth
        │
        ▼
Projected Circumference (t+1)
        │
        ▼
Projected DBH
        │
        ▼
Projected Biomass
        │
        ▼
Biomass Increment
        │
        ▼
Carbon Increment
        │
        ▼
Estimated CO₂ Sequestration Potential
```

---

# 1. Diameter at Breast Height (DBH)

Tree circumference was converted into diameter at breast height using:

<p>$$
D_i
=
\frac{C_i}{\pi}
$$

where:

- $C_i$ = Circumference of tree $i$
- $D_i$ = Diameter at Breast Height (DBH) of tree $i$

DBH is subsequently used as an input to the above-ground biomass allometric equation.

---

# 2. Above-Ground Biomass (AGB)

Above-ground biomass represents the biomass contained primarily in the stems and foliage of the trees.

The analysis uses the generalized pantropical allometric model proposed by **Chave et al. (2014)**.

The stem component is estimated using:

<p>$$
\text{AGB}_{\text{stems}}
=
\sum_{i=1}^{228}
\left(
\rho_i D_i^2 H_i
\right)^{0.976}
$$

where:

- $\rho_i$ = Wood density of species $i$
- $D_i$ = DBH of tree $i$, measured in metres
- $H_i$ = Tree height in metres
- $i$ = Individual tree index
- $n = 228$ = Total number of surveyed trees

The analysis also estimates foliage biomass as approximately 4% of stem biomass.

---

# 3. Below-Ground Biomass (BGB)

Below-ground biomass was not directly measured during the field survey.

Instead, it was estimated as a fixed proportion of above-ground biomass:

<p>$$
\text{BGB}
=
0.20 \times \text{AGB}
$$

Therefore:

<p>$$
\text{Total Biomass}
=
\text{AGB}+\text{BGB}
$$

or:

<p>$$
\text{Total Biomass}
=
1.20\times\text{AGB}
$$

This approach provides an estimate of root biomass based on the assumed below-ground-to-above-ground biomass ratio.

---

# 4. Carbon Stock

Carbon stock represents the amount of carbon stored in the estimated tree biomass.

A carbon fraction of **0.47** was applied to total dry biomass:

<p>$$
\text{Carbon Stock}
=
\text{Total Biomass}
\times 0.47
$$

Thus, the estimated carbon stock depends directly on the calculated total biomass and the assumed carbon fraction.

---

# 5. CO₂-Equivalent

The stored carbon was converted into the corresponding amount of atmospheric CO₂ using the molecular-weight ratio:

<p>$$
CO_{2e}
=
\text{Carbon}
\times
\frac{44}{12}
$$

where:

- $44$ = Molecular weight of CO₂
- $12$ = Atomic/molecular weight of carbon

Therefore:

<p>$$
1\text{ tonne C}
\approx
3.667\text{ tonnes CO}_2
$$

This converts the carbon stored in biomass into its equivalent quantity of atmospheric CO₂.

---

# 6. Age-Based Growth Projection

Direct annual remeasurement of the surveyed trees was not available.

Therefore, an age-based growth model was used to estimate subsequent-year tree growth.

The **Chapman–Richards growth function** was used to establish the relationship between tree age and circumference:

<p>$$
C
=
K
\left(
1-e^{-rA}
\right)^{1/m}
$$

where:

* (C) = tree circumference
* (A) = tree age
* (K), (r), and (m) = fitted growth parameters

The fitted relationship was used to estimate age for trees for which direct age observations were unavailable.

---

# 7. Annual Circumference Growth

The derivative of the Chapman–Richards function provides the estimated annual circumference growth rate:

<p>$$
\frac{dC}{dA}
$$

The circumference in the subsequent year was then estimated as:

<p>$$
C_{t+1}
=
C_t
+
\left(
\frac{dC}{dA}
\right)_t
$$

The projected circumference was converted back into DBH:

<p>$$
DBH_{t+1}
=
\frac{C_{t+1}}{\pi}
$$

The projected DBH was subsequently used to estimate next-year biomass.

---

# 8. Subsequent-Year Biomass

The projected DBH was used as an input to the allometric biomass model to obtain projected above-ground biomass.

The resulting sequence is:

<p>$$
C_{t+1}
\rightarrow
DBH_{t+1}
\rightarrow
AGB_{t+1}
\rightarrow
Biomass_{t+1}
$$

The annual biomass increment is:

<p>$$
\Delta Biomass
=
Biomass_{t+1}
-
Biomass_t
$$

The detailed calculation procedure is provided in the project appendix.

---

# 9. Carbon Sequestration Potential

The annual increase in biomass was converted into an increase in carbon stock:

<p>$$
\Delta C
=
\Delta Biomass
\times
CF
$$

where:

<p>$$
CF = 0.47
$$

The corresponding CO₂ sequestration potential was then estimated as:

<p>$$
\Delta CO_2
=
\Delta C
\times
\frac{44}{12}
$$

Therefore, the final estimation chain is:

<p>$$
\Delta Biomass
\rightarrow
\Delta Carbon
\rightarrow
\Delta CO_2
$$

This represents a **model-based estimated annual CO₂ sequestration potential**, rather than directly observed annual sequestration.

---

# Key Results

The field survey covered **228 trees belonging to 19 species**.

Based on the detailed results table, the estimated current biomass and carbon stock were:

| Measure                                      |       Estimated value |
| -------------------------------------------- | --------------------: |
| Number of trees                              |                   228 |
| Number of species                            |                    19 |
| Above-ground biomass                         |          1,805.431 kg |
| Below-ground biomass                         |            361.086 kg |
| Total biomass                                |          2,166.517 kg |
| Current carbon stock                         |        1,018.263 kg C |
| Stored CO₂-equivalent                        |     3,733.631 kg CO₂e |
| Projected biomass at (t+1)                   |          2,931.586 kg |
| Estimated annual CO₂ sequestration potential | 1,318.468 kg CO₂/year |

## The detailed species-level results are reported in the study's Results section.

# Species-Level Results

Carbon storage was unevenly distributed across species.

The major contributors to current carbon stock and estimated sequestration potential include:

| Species               | Trees | Current Carbon Stock (kg C) | CO₂e Stored (kg) | CO₂ Sequestration Potential |
| --------------------- | ----: | --------------------------: | ---------------: | --------------------------: |
| Polyalthia longifolia |   102 |                     304.313 |        1,115.816 |                     476.588 |
| Ficus religiosa       |     3 |                     183.197 |          671.722 |                     148.004 |
| Azadirachta indica    |    32 |                     144.218 |          528.799 |                     195.995 |
| Syzygium cumini       |    14 |                      79.393 |          291.107 |                      97.064 |
| Borassus flabellifer  |     6 |                      92.198 |          338.058 |                      84.941 |
| Dalbergia sissoo      |     8 |                      60.058 |          220.211 |                      62.176 |
| Mangifera indica      |    21 |                      46.652 |          171.059 |                      76.604 |
| Tectona grandis       |     8 |                      34.962 |          128.193 |                      46.063 |

Among the surveyed species, **Polyalthia longifolia** was both the most abundant species and the largest contributor to estimated carbon stock and sequestration potential.

---

# Key Finding

### Polyalthia longifolia

Polyalthia longifolia accounted for:

* **102 of the 228 surveyed trees**
* Approximately **304.31 kg of current carbon stock**
* Approximately **1,115.82 kg CO₂-equivalent stored**
* Approximately **476.59 kg CO₂/year of estimated sequestration potential**

This illustrates how both **tree abundance and individual-tree biomass** influence the overall contribution of a species to a local carbon sink.

---

# Carbon Stock vs. Sequestration Potential

These two concepts are distinct:

### Carbon Stock

Carbon stock represents the carbon **already stored** in the existing tree biomass at the time of assessment.

### Sequestration Potential

Sequestration potential represents the **estimated additional carbon storage associated with future tree growth**.

Therefore:

```text
Carbon Stock
= Carbon already stored

Sequestration Potential
= Estimated additional storage through growth
```

The project does not interpret the estimated annual sequestration value as directly observed annual carbon removal.

---

# Growth Projection Framework

The age-based growth component follows:

```text
Observed Age–Circumference Data
              │
              ▼
     Chapman–Richards Model
              │
              ▼
      Estimate Tree Age
              │
              ▼
     Estimate dC / dA
              │
              ▼
    Circumference at t+1
              │
              ▼
        DBH at t+1
              │
              ▼
      Biomass at t+1
              │
              ▼
       Biomass Increment
              │
              ▼
       Carbon Increment
              │
              ▼
  Estimated CO₂ Sequestration
```

This modelling approach was adopted because direct annual remeasurement of the same trees was not available.

---

# Visualizations

The project includes visual analysis of:

* Species distribution
* Carbon stock by species
* CO₂ sequestration potential by species
* Current versus projected biomass
* Age–circumference relationship
* Chapman–Richards growth curve

The growth analysis compares the theoretical growth relationship with observed age–DBH information from the Hall-8 dataset.

---

# Reproducibility

The original analysis was performed using spreadsheet-based calculations.

The GitHub version is organized to make the analysis easier to inspect and reproduce.

The planned analytical workflow is:

```text
Raw Field Data
      │
      ▼
Data Cleaning
      │
      ▼
DBH Calculation
      │
      ▼
AGB Calculation
      │
      ▼
BGB Calculation
      │
      ▼
Total Biomass
      │
      ▼
Carbon Stock
      │
      ▼
CO₂ Equivalent
      │
      ▼
Growth Model
      │
      ▼
Projected Biomass
      │
      ▼
Estimated Sequestration
      │
      ▼
Visualization & Results
```

The Python implementation, if included in this repository, is intended to reproduce and validate the spreadsheet-based calculations rather than replace the original field analysis.

---

# Repository Structure

```text
hall-8-carbon-sequestration/
│
├── README.md
│
├── data/
│   └── Hall8_Tree_Inventory.xlsx
│
├── google_sheets/
│   └── Hall8_Carbon_Analysis.xlsx
│
├── notebooks/
│   └── carbon_sequestration_analysis.ipynb
│
├── src/
│   └── carbon_sequestration.py
│
├── results/
│   ├── species_carbon_stock.csv
│   ├── sequestration_results.csv
│   │
│   └── figures/
│       ├── biomass_by_species.png
│       ├── carbon_stock_by_species.png
│       ├── co2_sequestration_by_species.png
│       └── growth_curve.png
│
├── report/
│   └── Final_Report.pdf
│
└── presentation/
    └── Presentation.pdf
```

### Directory Description

| Directory          | Purpose                                      |
| ------------------ | -------------------------------------------- |
| `data/`            | Raw/cleaned tree inventory data              |
| `google_sheets/`   | Original spreadsheet-based analysis          |
| `notebooks/`       | Exploratory and reproducible Python analysis |
| `src/`             | Reusable Python calculation functions        |
| `results/`         | Processed results and exported outputs       |
| `results/figures/` | Project visualizations                       |
| `report/`          | Final academic report                        |
| `presentation/`    | Project presentation                         |

---

# Limitations

The estimated carbon stock and sequestration potential should be interpreted as model-based estimates.

Important limitations include:

### 1. Measurement Error

The estimates depend on the accuracy of:

* Circumference measurements
* DBH calculations
* Tree-height measurements
* Species identification
* Wood-density values

### 2. Allometric Model Assumptions

Biomass estimates depend on the selected allometric equation and its applicability to the surveyed trees.

### 3. Below-Ground Biomass Assumption

BGB was estimated as 20% of AGB rather than being directly measured.

### 4. Carbon Fraction

A carbon fraction of 0.47 was applied to total dry biomass.

### 5. Growth Projection

Annual growth was estimated using an age-based growth function because direct annual remeasurement was unavailable.

### 6. Tree Selection

Trees with circumference below 8 cm were excluded from the analysis.

### 7. Estimated Rather Than Observed Sequestration

The reported annual CO₂ sequestration figure is a **model-based potential**. Re-measuring the same trees after one or more years would provide a more robust estimate of actual annual biomass growth and carbon sequestration.

---

# Interpretation

The results indicate that the Hall-8 tree population represents a measurable local carbon sink.

The carbon stock is strongly influenced by both:

1. The number of trees belonging to a species, and
2. The biomass of individual trees.

This explains why Polyalthia longifolia, despite being one species among 19, makes a particularly large contribution to the overall carbon stock because it accounts for 102 of the surveyed trees.

The growth-based projection additionally provides a framework for estimating how continued tree growth could contribute to future carbon storage.

---

# Technical Skills Demonstrated

This project demonstrates the application of:

* Primary field-data collection
* Data cleaning and organization
* Quantitative data analysis
* Biomass estimation
* Allometric modelling
* Carbon-stock estimation
* CO₂-equivalent conversion
* Nonlinear growth modelling
* Chapman–Richards growth function
* Mathematical differentiation
* Growth projection
* Species-level aggregation
* Data visualization
* Spreadsheet-based analytical modelling
* Reproducible Python analysis

---

# Methodological Framework

The overall analytical framework can be summarized as:

<p>$$
C
\rightarrow
DBH
\rightarrow
AGB
\rightarrow
BGB
\rightarrow
\text{Total Biomass}
\rightarrow
\text{Carbon}
\rightarrow
CO_2e
$$

For future growth:

<p>$$
Age
\rightarrow
Circumference
\rightarrow
C_{t+1}
\rightarrow
DBH_{t+1}
\rightarrow
Biomass_{t+1}
\rightarrow
\Delta Biomass
\rightarrow
\Delta Carbon
\rightarrow
\Delta CO_2
$$

---

# Academic References

### Chave et al. (2014)

Chave et al. (2014) — Generalized pantropical allometric model used for above-ground biomass estimation.

### Richards (1959)

Richards, F. J. (1959). *A flexible growth function for empirical use*. Journal of Experimental Botany, 10(2), 290–300. DOI: 10.1093/jxb/10.2.290.

### MacDicken (1997)

MacDicken, K. G. (1997). *A Guide to Monitoring Carbon Storage in Forestry and Agroforestry Projects*. Winrock International.

### IPCC (2006)

IPCC (2006). *2006 IPCC Guidelines for National Greenhouse Gas Inventories*. Volume 4: Agriculture, Forestry and Other Land Use.

### Puc-Kauil et al. (2020)

Puc-Kauil, R. et al. (2020). iForest, 13, 165–174. DOI: 10.3832/ifor3167-013.

The references above correspond to the methodological sources cited in the project report.

---

# Report and Presentation

The complete academic report is available in:

```text
report/Final_Report.pdf
```

The project presentation is available in:

```text
presentation/Presentation.pdf
```

## The presentation provides a visual summary of the field inventory, biomass methodology, growth projection, and sequestration estimation workflow.

# AI Tools Disclosure

AI tools were used during preparation of the academic report for purposes including:

* Literature-search assistance
* Understanding carbon-sequestration concepts
* Organizing the report structure
* Checking mathematical formulations
* Improving language and presentation

The field data, measurements, assumptions, calculations, and interpretation were collected, performed, and/or verified by the researcher, with AI-generated information cross-checked against relevant academic and institutional sources.

---

# Author

**Durgesh Yadav**

M.Sc. Economics
Indian Institute of Technology Kanpur

---

# Project Status

**Completed — Academic Research Project**

The field inventory, biomass estimation, carbon-stock estimation, growth projection, and estimated sequestration analysis have been completed.

The GitHub repository additionally provides a reproducible computational implementation of the spreadsheet-based analysis where applicable.
