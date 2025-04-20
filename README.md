# 📊 Comparative Study of Clustering Algorithms using Preprocessing Techniques

## 📌 Overview

This project presents a comparative performance study of different **clustering algorithms** using various **pre-processing techniques** on a small dataset from the UCI repository. The goal is to observe how clustering performance varies based on:

- The algorithm used
- Preprocessing applied
- Number of clusters chosen
- Evaluation metrics

## 📁 Dataset

- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wine)
- **Dataset Used:** 🍷 **Wine Dataset**
- **Description:** This dataset contains the results of a chemical analysis of wines grown in the same region in Italy but derived from three different cultivars.
- **Features:** 13 numerical attributes
- **Target:** Wine class (not used in unsupervised clustering)
- **Preprocessing:** Normalization, Transformation, PCA, and combinations

## 🧠 Clustering Algorithms

- **KMeans Clustering**
- **Hierarchical Clustering**
- **MeanShift Clustering**

## ⚙️ Preprocessing Techniques

- **None** – Raw data
- **Normalization** – MinMax Scaling
- **Transform** – e.g., Log, Power Transform
- **PCA** – Dimensionality Reduction
- **T+N** – Transform + Normalize
- **T+N+PCA** – All combined

## 📐 Evaluation Metrics

- **Silhouette Score** – Higher is better
- **Calinski-Harabasz Index** – Higher is better
- **Davies-Bouldin Score** – Lower is better

## 📊 Results Summary

| Method        | Preprocessing | Clusters | Silhouette | Calinski-Harabasz | Davies-Bouldin |
|---------------|---------------|----------|------------|--------------------|----------------|
| KMeans        | No Preprocessing | 3 | 0.571 | 562 | 0.53 |
| KMeans        | No Preprocessing | 4 | 0.545 | 600 | 0.56 |
| KMeans        | No Preprocessing | 5 | 0.548 | 727 | 0.54 |
| KMeans        | Normalization    | 3 | 0.285 | 71  | 1.39 |
| KMeans        | Normalization    | 4 | 0.286 | 54  | 1.49 |
| KMeans        | Normalization    | 5 | 0.245 | 46  | 1.69 |
| KMeans        | Transform        | 3 | 0.301 | 73  | 1.36 |
| KMeans        | Transform        | 4 | 0.236 | 53  | 1.71 |
| KMeans        | Transform        | 5 | 0.210 | 46  | 1.96 |
| KMeans        | PCA              | 3 | 0.572 | 563 | 0.53 |
| KMeans        | PCA              | 4 | 0.546 | 601 | 0.56 |
| KMeans        | PCA              | 5 | 0.549 | 729 | 0.54 |
| KMeans        | T+N              | 3 | 0.301 | 73  | 1.36 |
| KMeans        | T+N              | 4 | 0.236 | 53  | 1.71 |
| KMeans        | T+N              | 5 | 0.210 | 46  | 1.96 |
| KMeans        | T+N+PCA          | 3 | 0.573 | 351 | 0.59 |
| KMeans        | T+N+PCA          | 4 | 0.479 | 281 | 0.76 |
| KMeans        | T+N+PCA          | 5 | 0.472 | 305 | 0.79 |
| Hierarchical  | No Preprocessing | 3 | 0.564 | 553 | 0.54 |
| Hierarchical  | No Preprocessing | 4 | 0.561 | 671 | 0.55 |
| Hierarchical  | No Preprocessing | 5 | 0.507 | 684 | 0.55 |
| Hierarchical  | Normalization    | 3 | 0.277 | 68  | 1.42 |
| Hierarchical  | Normalization    | 4 | 0.226 | 51  | 1.79 |
| Hierarchical  | Normalization    | 5 | 0.187 | 44  | 1.92 |
| Hierarchical  | Transform        | 3 | 0.290 | 69  | 1.39 |
| Hierarchical  | Transform        | 4 | 0.252 | 53  | 1.70 |
| Hierarchical  | Transform        | 5 | 0.229 | 45  | 1.81 |
| Hierarchical  | PCA              | 3 | 0.566 | 554 | 0.53 |
| Hierarchical  | PCA              | 4 | 0.562 | 672 | 0.55 |
| Hierarchical  | PCA              | 5 | 0.501 | 685 | 0.56 |
| Hierarchical  | T+N              | 3 | 0.290 | 69  | 1.39 |
| Hierarchical  | T+N              | 4 | 0.252 | 53  | 1.70 |
| Hierarchical  | T+N              | 5 | 0.229 | 45  | 1.81 |
| Hierarchical  | T+N+PCA          | 3 | 0.557 | 320 | 0.61 |
| Hierarchical  | T+N+PCA          | 4 | 0.474 | 297 | 0.76 |
| Hierarchical  | T+N+PCA          | 5 | 0.443 | 303 | 0.85 |
| MeanShift     | No Preprocessing | 4 | 0.582 | 351 | 0.45 |
| MeanShift     | Normalization    | 6 | 0.221 | 19  | 0.98 |
| MeanShift     | Transform        | 2 | 0.110 | 8   | 2.01 |
| MeanShift     | PCA              | 4 | 0.582 | 351 | 0.45 |
| MeanShift     | T+N              | 2 | 0.110 | 8   | 2.01 |
| MeanShift     | T+N+PCA          | 4 | 0.499 | 329 | 0.75 |

---

## 📈 Visualizations


### 📊 Silhouette Scores 
![Silhouette Score](/silhoutte)

### 🧬 Calinski-Harabasz Index
![Calinski-Harabasz Index](/calinski)

### 🧮 Davies-Bouldin
![Davies-Bouldin Score](davis)


---

## ✅ Key Insights

- **KMeans with PCA or T+N+PCA** provided consistently high performance on all metrics.
- **Hierarchical Clustering** also performed well with PCA and full preprocessing.
- **MeanShift** was effective on raw/PCA data but computationally heavy and less consistent post-transformation.
- Excessive preprocessing (like T+N) without PCA often led to poor clustering performance.

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/clustering-comparison.git
