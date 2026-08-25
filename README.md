# Sectoral Segmentation using Clustering Techniques
### Indian Financial Services Sector

## Overview
This project uses clustering to segment 50 companies in the Indian Financial Services sector based on financial performance — profitability, liquidity, growth, and efficiency.

## Data
`Finance.csv` — 7 financial ratios per company: ROE, ROA, Current Ratio, Quick Ratio, Revenue Growth (1Y), Basic EPS, Total Asset Turnover. Features are scaled with MinMax normalization before clustering.

## Approach
1. EDA (distributions, boxplots, correlation heatmap)
2. Find optimal K (Elbow Method, Silhouette Score, CH Score)
3. K-Means clustering (K = 3)
4. Feature importance (ANOVA F-score)
5. Hierarchical clustering (Ward linkage) to validate results
6. HDBSCAN to flag outlier firms

## Results
**Best K = 3** (Silhouette = 0.508, CH = 29.62)

- **Cluster 0:** Diversified firms — moderate profitability & liquidity, stable growth
- **Cluster 1:** High-performing asset management/securities firms — very high ROE, ROA, efficiency
- **Cluster 2:** Investment-oriented firms — high liquidity & EPS, lower growth/efficiency

**Top drivers of clustering:** Return on Assets, Return on Equity, Basic EPS

## Files
- `Sectoral_Segmentation_using_Clustering_Techniques.ipynb` — analysis notebook
- `Sectoral_Segmentation_using_Clustering_Techniques.pdf` — written report
- `Finance.csv` — dataset (required to run notebook)

## Run it
```bash
pip install pandas numpy matplotlib seaborn scikit-learn yellowbrick
```
Place `Finance.csv` alongside the notebook and run top to bottom.
