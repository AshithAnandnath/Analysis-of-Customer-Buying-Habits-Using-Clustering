# Analysis of Customer Buying Habits Using Clustering

Unsupervised customer segmentation on a retail shopping dataset — cleaning, EDA, and K-Means clustering to identify distinct buyer personas that could support targeted marketing.

## Problem Statement
Retail customers differ widely in spending habits, shopping frequency, and discount sensitivity. Understanding these differences helps a business improve customer satisfaction, increase sales, and design targeted campaigns.

## What this notebook does
- Cleans and encodes a customer shopping habits dataset (categorical encoding, scaling)
- Runs exploratory data analysis and correlation checks on spending behavior
- Selects features and uses the **Elbow Method** to choose the optimal number of clusters
- Segments customers with **K-Means**, then visualizes clusters with **PCA**
- Validates cluster separation with confidence intervals and hypothesis testing
- Profiles each segment and turns them into business-readable personas

## Key Findings
- The Elbow Method identified **K = 3** as the optimal number of clusters
- **Cluster 0 — Frequent Budget Customers**: buy often, spend less per transaction
- **Cluster 1 — High Value Customers**: highest overall spend and purchase activity
- **Cluster 2 — Young Moderate Spenders**: moderate spend, strongest growth potential
- Age, purchase amount, previous purchases, review ratings, and purchase frequency were the strongest drivers of segment membership

## Limitations
- Single dataset, no income/occupation data, no external market factors
- K-Means assumes roughly spherical clusters, which may not hold for all real customer behavior
- Segments are a snapshot — customer behavior can drift over time

## Tech Stack
Python · pandas · NumPy · scikit-learn (KMeans, StandardScaler, PCA) · matplotlib · seaborn

## How to run
Open `notebook.ipynb` in Jupyter or Google Colab and run cells top to bottom. Dataset: `CustomerShoppingHabits.csv` (place in the working directory / mount to `/content` if using Colab).
