# vienna-pharmacy-geospatial-analysis
## Project Overview

This project investigates how pharmacies are distributed across Vienna's 23 districts and whether population density is associated with pharmacy clustering and geographic isolation.

The analysis combines pharmacy location data with district-level population statistics to identify geographic patterns and investigate potential accessibility concerns.

## Research Questions

1. How are pharmacies distributed across Vienna?
2. Is the number of pharmacies associated with district population?
3. Which pharmacies are geographically isolated?
4. Is population density associated with pharmacy isolation?
5. Which districts warrant further accessibility investigation?

## Dataset

The analysis uses:

- **[Pharmacy locations](https://www.data.gv.at/datasets/cf00fe06-e4b2-4319-af00-85230e7b2f1b?locale=de):** 358 pharmacies across Vienna's 23 districts. link: 
- **[Population data](https://data.wien.gv.at/):** District-level population statistics.
- **Population density:** Residents per square kilometer for each district in 2025 (Statatlas).

## Technologies and Methods

**Python:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy, and PyProj.

**Analysis techniques:**
- Exploratory Data Analysis (EDA)
- Pearson and Spearman correlation
- K-Means clustering
- DBSCAN clustering
- Silhouette Score and cross-validation

## Key Findings

### 1. Pharmacy Distribution and Population

We found a **strong positive correlation (Pearson's r ≈ 0.84)** between district population and the number of pharmacies.

More populated districts generally have more pharmacies.

### 2. Geographic Clustering

K-Means identified **two broad geographic clusters**, but was less suitable for detecting isolated pharmacies.

DBSCAN was used to investigate local pharmacy clustering and geographic isolation.

The preliminary analysis identified **33 pharmacies (9.22%)** as noise, indicating locations outside dense pharmacy clusters.

### 3. Population Density and Isolation

We found a **strong negative correlation (Spearman's ρ ≈ −0.80)** between population density and the percentage of pharmacies classified as noise.

This suggests that pharmacies in less densely populated districts tend to be more geographically isolated.

These results support an association between population density and pharmacy isolation, but do not establish causation.


## Conclusion

The analysis shows that district population is strongly associated with pharmacy counts, while population density is negatively associated with geographic pharmacy isolation.

These findings provide a foundation for more detailed accessibility research, particularly for identifying areas that may benefit from improved pharmacy coverage (details for future work on the pharmacy notebook).
