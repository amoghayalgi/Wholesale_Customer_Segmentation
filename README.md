# Wholesale Customer Segmentation Analysis

This repository contains a comprehensive analysis of the **Wholesale Customers dataset**, applying unsupervised machine learning techniques to segment customers based on annual spending patterns.

---

## Project Overview

The primary goal of this project is to identify distinct customer segments to help a Portuguese wholesale distributor:

- Optimize inventory management  
- Tailor marketing strategies  
- Improve overall profitability  

By analyzing spending across product categories such as:

- Fresh  
- Milk  
- Grocery  
- Frozen  
- Detergents/Paper  
- Delicatessen  

this project provides a **data-driven foundation for strategic decision-making**.

---

## Business Questions

### Segmentation
- What are the distinct customer segments based on annual spending behavior?

### Demographics
- How do segments differ across:
  - Sales Channels (HoReCa vs Retail)
  - Regions (Lisbon, Oporto, Other)

### Optimization
- Which product categories drive spending within each segment?
- Where can targeted strategies (discounts, bundling) improve profitability?

---

## Methodology

The analysis follows a structured data science workflow implemented in **R**:

### 1. Data Preprocessing
- Normalized spending values to a **0–1 scale**
- Prevented high-value categories from dominating clustering

---

### 2. Hierarchical Clustering
- Used to explore natural groupings
- Dendrogram analysis estimated cluster count as 3

---

### 3. K-Means Clustering
- Applied with **k = 3**
- Validated k-value using:
  - Elbow Method (SSE)
  - Silhouette Score
- Finalized k-means clusters K-means because it defines distinct segments by their average spending patterns (centroids)

---

### 4. Principal Component Analysis (PCA)
- Reduced dimensionality
- Enabled visualization of clusters in 2D space

---

## Identified Customer Segments

| Segment              | Primary Characteristics                                      | Strategy Focus |
|---------------------|-------------------------------------------------------------|--------------|
| **Retail Customers** | High spending in Grocery, Milk, Detergents                  | Loyalty programs, private-label staples |
| **High-Spend HoReCa** | Heavy spending on Fresh products                           | Logistics optimization, perishables management |
| **Low-Spend HoReCa** | Lower, varied spending across categories                    | Bundling strategies ("Chef Kits") |

---

## Strategic Recommendations

### Micro-Supply Chains
- Separate systems:
  - **Dry/Dairy** for Retail
  - **Perishables** for HoReCa  
- Reduces spoilage and improves delivery efficiency

---

### SKU Optimization
- Apply **Pareto Principle (80/20 rule)**
- Remove low-performing items (<1% contribution)
- Focus on high-demand products per segment

---

### Private Label Strategy
- Launch **5–7 private-label staples**
- Price slightly below national brands
- Increase margins and customer retention

---

## Project Structure
├── code/ # R scripts for preprocessing, clustering, and PCA
├── data/ # Raw and processed dataset files
├── visualizations/ # Post-hoc analysis, plots, and results
---

## Technologies Used

```r
library(dplyr)    # Data manipulation
library(cluster)  # Clustering algorithms (Hierarchical & K-Means)
library(ggplot2)  # Data visualization
library(tidyr)    # Data cleaning

```

