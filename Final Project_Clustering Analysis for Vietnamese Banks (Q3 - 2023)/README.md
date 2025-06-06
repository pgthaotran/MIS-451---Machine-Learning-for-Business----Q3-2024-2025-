# Clustering Analysis for Vietnamese Banks (Q3 - 2023)

## Project Overview

This project presents a data-driven approach to segment Vietnamese banks into meaningful peer groups based on their financial performance in the third quarter of 2023. Using machine learning clustering techniques, this analysis identifies homogeneous segments within the banking sector, uncovers strategic patterns, and provides a foundation for tailored strategic recommendations.

The primary methods employed are **K-Means Clustering** and **Hierarchical Clustering**, with **Principal Component Analysis (PCA)** used for dimensionality reduction and visualization.

## Business Problem

Vietnam's banking industry is highly diverse, with institutions varying significantly in scale, profitability, operational focus, and risk profiles. This diversity makes direct performance comparison and strategic benchmarking challenging for regulators, investors, and the banks themselves. This project addresses this gap by creating a standardized segmentation based on key financial indicators.

**Objective:** To apply clustering algorithms to segment 27 Vietnamese banks using their Income Statement (KQKD) metrics from Q3 2023, and derive strategic insights from the resulting clusters.

## Dataset

* **Source:** `BCTC_Bank.xlsx` - A dataset containing financial metrics for Vietnamese banks.
* **Scope:** The analysis is scoped to financial data from **Q3 2023** for **27 unique banks**.
* **Features:** We focused on **21 key financial indicators** from the Income Statement (known as "KQKD" metrics). These metrics were chosen because they directly reflect a bank's profitability and operational efficiency.

## Methodology

The project follows a standard data science workflow:

1.  **Data Preparation:**
    * **Filtering & Selection:** Isolated data for Q3 2023 and selected relevant KQKD (Income Statement) metrics.
    * **Data Transformation (Pivoting):** Restructured the data from a long format to a wide format, where each bank is an observation and each financial metric is a feature.
    * **Feature Standardization:** Applied `StandardScaler` to normalize the feature values. This step is crucial for distance-based algorithms like K-Means to ensure all metrics contribute fairly to the analysis, regardless of their original scale.

2.  **K-Means Clustering:**
    * **Optimal Cluster Selection:** Used the **Elbow Method** and **Silhouette Score Analysis** to determine the optimal number of clusters, which was found to be **3**.
    * **Segmentation:** Grouped the 27 banks into three distinct clusters based on their financial profiles.

3.  **Hierarchical Clustering:**
    * **Alternative Method:** Employed Ward's linkage method as a secondary approach to validate the groupings.
    * **Dendrogram Analysis:** Visualized the cluster hierarchy with a dendrogram, which also supported the formation of 3 primary clusters.

4.  **Visualization (PCA):**
    * **Dimensionality Reduction:** Used Principal Component Analysis (PCA) to reduce the 21 financial metrics into two principal components, capturing the majority of the data's variance.
    * **2D Scatter Plots:** Visualized the bank clusters on 2D plots to visually inspect their separation and positioning.

## Files in this Repository

* `MIS451_FINAL_PROJECT_CLUSTERING.ipynb`: The main Jupyter Notebook containing all Python code and analysis.
* `BCTC_Bank.xlsx`: The raw dataset used for the analysis.
* `MIS451_FINAL_PROJECT_REPORT.pdf`: The comprehensive final report detailing the project's methodology, findings, and conclusions.
* `MIS451_FINAL_PROJECT_PRESENTATION.pdf`: The slide deck for the project presentation.

