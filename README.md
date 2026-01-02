# README — Figures (LAC & SSA Mobility, Collaboration and Position)

This repository/script generates the **Figure set (Figure 1–Figure 9)** for the analysis of publication output, researcher counts, international mobility, collaboration patterns, authorship positions, and spatial “center of gravity” of mobility destinations for **Latin America & Caribbean (LAC)** and **Sub-Saharan Africa (SSA)**.

## 1. Overview of outputs

The script produces the following PNG files:

- **Figure 1--pub_researcher_region_year.png**  
  Bars: total publications and total researchers (LAC vs SSA) by year.  
  Points (secondary axis): average publications per researcher.

- **Figure  2--mobility_LAC.png**  
  Line plot of mobility flows **to/from LAC** by partner region (counts).

- **Figure  3--mobility_SSA.png**  
  Line plot of mobility flows **to/from SSA** by partner region (counts).

- **Figure  4--moblity network-combine--SSA-LAC.png**  
  A 2×2 combined image (cropped + annotated) of four Gephi network snapshots
  for different time periods.

- **Figure 5--quah--SSA--LAC--central of gravity of mobility destinaiton--across region of origin.png**  
  Trajectories of destination “center of gravity” (Quah-style) over time for LAC vs SSA.

- **Figure  6--coll_LAC.png**  
  Collaboration trends for LAC by field and collaboration partner type (counts + proportions).

- **Figure  7--coll_SSA.png**  
  Collaboration trends for SSA by field and collaboration partner type (counts + proportions).

- **Figure  8--first_last_SSA.png**  
  Time trends of first vs last authorship shares in SSA collaborations by partner region.

- **Figure  9--first_last_LAC.png**  
  Time trends of first vs last authorship shares in LAC collaborations by partner region.

> Notes:  
> - In mobility and collaboration plots, a dashed vertical line at **2020** is used as a reference point (e.g., COVID-era boundary).  
> - Many plots use `scales = "free_y"` in faceting to allow different magnitudes across panels.

---

## 2. Required software

- **R** (recommended: R 4.2+)
- Recommended: **RStudio**

---

## 3. R packages

The script uses (at least) the following packages:

- Data handling: `dplyr`, `tidyr`
- Plotting: `ggplot2`, `ggrepel`, `grid`, `gridExtra`, `gtable`
- Inequality measures: `ineq`
- Spatial and geographic tools: `geosphere`, `sf`, `maps` (via `map_data("world")`)
- Image processing: `png`, `magick`
- Others (loaded but not necessarily used in every block): `MASS`, `networkD3`, `htmltools`, `ggalluvial`, `pracma`

Install missing packages in R:

```r
install.packages(c(
  "dplyr","tidyr","ggplot2","ggrepel","ineq","geosphere","sf",
  "gridExtra","gtable","png","magick","pracma","MASS","networkD3","htmltools","ggalluvial","maps"
))
