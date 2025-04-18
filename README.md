# Clustering Assignment: Comparative Study of Clustering Algorithms

## 📋 Overview

This repository contains a comparative performance study of different clustering algorithms using various pre-processing techniques on a small UCI dataset. We evaluate each combination across three standard clustering metrics and identify the best-performing configuration.

## 🗂 Dataset

- **Name:** Iris
- **Link:** [https://archive.ics.uci.edu/ml/datasets/iris](https://archive.ics.uci.edu/ml/datasets/iris)
- **Number of Features:** 4
- **Number of Rows:** 150

## 🔧 Pre-processing Techniques

We applied the following pre-processing pipelines to the feature matrix:

1. **None** (raw data)
2. **Min-Max Normalization**
3. **Power Transformation**
4. **Principal Component Analysis (PCA)**
5. **Min-Max + Power**
6. **Min-Max + PCA**

## 🤖 Clustering Algorithms

- **KMeans**
- **Agglomerative Clustering**
- **Mean Shift**

## 📏 Evaluation Metrics

For each clustering result, we computed:

- **Silhouette Score**
- **Calinski–Harabasz Index**
- **Davies–Bouldin Index**

## 📊 Results Summary

| Pre-processing | Algorithm                | # Clusters | Silhouette | Calinski–Harabasz | Davies–Bouldin |
| -------------- | ------------------------ | ---------- | ---------- | ----------------- | -------------- |
| None           | Agglomerative Clustering | 2          | 0.68639    | 501.92            | 0.3836         |
| None           | Mean Shift               | 2          | 0.68548    | 508.88            | 0.3893         |
| None           | KMeans                   | 2          | 0.68081    | 513.30            | 0.4048         |
| …              | …                        | …          | …          | …                 | …              |

> **Best Configuration:**
>
> - **Algorithm:** Agglomerative Clustering
> - **# Clusters:** 2
> - **Silhouette Score:** 0.68639

*Full result tables and plots are available in the **`results/`** directory.*

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/your-username/your-repo.git
cd your-repo

# Install dependencies
pip install -r requirements.txt

# Launch the notebook (locally or in Colab)
jupyter notebook Clustering_Assignment.ipynb
```

## 📂 Repository Structure

```
├── Clustering_Assignment.ipynb   # Jupyter/Colab notebook with code, tables, and plots
├── requirements.txt              # Python dependencies
├── README.md                     # This overview
├── results/                      # Folder with detailed CSVs and images
│   ├── tables/
│   │   └── full_metrics_table.csv
│   └── plots/
│       ├── kmeans_silhouette.png
│       └── ...
└── data/                         # (optional) raw data files if stored locally
```

## 📜 License

This project is released under the MIT License. Feel free to use and adapt as needed.

