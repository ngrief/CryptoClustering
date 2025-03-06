# Crypto Clustering

## Overview
This project applies **unsupervised learning** techniques to cluster cryptocurrencies based on their price changes over time. Using **K-Means clustering** and **Principal Component Analysis (PCA)**, the project identifies patterns in the cryptocurrency market and visualizes the results.

## Dataset
The dataset used for this analysis is located in the `Resources` folder:
```
Resources/crypto_market_data.csv
```
It contains various price change percentages for different cryptocurrencies.

## Goals
1. **Prepare the Data**
   - Load and clean the dataset.
   - Normalize the data using `StandardScaler`.
2. **Find the Best Value for k (Elbow Method)**
   - Compute inertia values for `k = 1 to 11`.
   - Plot the **Elbow Curve** to determine the optimal number of clusters.
3. **Cluster Cryptocurrencies Using K-Means**
   - Initialize and fit K-Means using the best `k`.
   - Predict cluster assignments.
   - Create a scatter plot of clusters based on `price_change_percentage_24h` vs. `price_change_percentage_7d`.
4. **Optimize Clustering with PCA**
   - Reduce the dataset to **3 principal components**.
   - Retrieve **explained variance** to evaluate information retention.
   - Re-run the Elbow Method on the PCA-transformed data.
5. **Cluster Cryptocurrencies Using PCA Data**
   - Fit and predict K-Means on PCA-reduced data.
   - Create a scatter plot of clusters using **PC1** and **PC2**.
6. **Compare Original vs PCA-Based Clustering**
   - Composite **Elbow Curve Plot** (Original vs PCA data).
   - Composite **Cluster Visualization** (Original vs PCA data).

## Files
- `Crypto_Clustering.ipynb` → Jupyter Notebook with full analysis and visualizations.
- `Resources/crypto_market_data.csv` → Raw cryptocurrency market data.

## Results
- **Best k for clustering** is determined using the Elbow Method.
- **Total Explained Variance of PCA** is calculated.
- **Cluster assignments are visualized** before and after PCA transformation.
- **Impact of PCA on clustering** is analyzed.

## Dependencies
To run this project, install the required Python libraries:
```bash
pip install pandas scikit-learn hvplot matplotlib bokeh
```

## Execution
Run the Jupyter Notebook `Crypto_Clustering.ipynb` step-by-step to reproduce the results.

## Insights
- PCA improves efficiency but may slightly alter cluster boundaries.
- K-Means is effective in grouping cryptocurrencies based on price behavior.
- Visualizations confirm patterns in the data, assisting in market analysis.

## Repository Structure
```
CryptoClustering/
│── Crypto_Clustering.ipynb   # Main Jupyter Notebook
│── Resources/
│   ├── crypto_market_data.csv  # Dataset
│── README.md                 # Project Documentation
└── requirements.txt          # Dependencies (optional)
```

## Author
- **Nathaniel Trief**

## License
This project is for educational purposes and is open-source.

