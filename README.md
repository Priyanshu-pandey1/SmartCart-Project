# SmartCart Clustering System 🛒

**SmartCart** is a data-driven customer segmentation project designed to identify distinct consumer behaviors using unsupervised learning. By analyzing demographics and purchasing patterns, this system categorizes customers into four primary segments, enabling businesses to tailor marketing strategies and optimize customer retention.

---

### 🚀 Project Overview
This project transforms raw customer data into actionable insights. The pipeline covers the entire data science lifecycle, from rigorous preprocessing to final cluster profiling using **Agglomerative Clustering**.

### 🛠️ Key Steps Performed
* **Data Cleaning:** Handled missing values and identified/removed outliers to ensure model robustness.
* **EDA & Visualization:** Generated **Heatmaps** to identify feature correlations and visualized data distributions.
* **Feature Engineering:** Created derived features like `Total_Spending`, `Total_Children`, and `Customer_Tenure_Days`.
* **Preprocessing:** Implemented **Feature Encoding** (Label/One-Hot) and **Scaling** for numerical features.
* **Optimal K Selection:** Used the **Elbow Method** and **Silhouette Score** to determine that **k=4** provides the most cohesive clusters.
* **Dimensionality Reduction:** Applied **PCA** (Principal Component Analysis) before clustering to improve performance.
* **Model Implementation:** Utilized **Agglomerative Clustering** with a "ward" linkage approach.

---

### 📊 Cluster Summary & Profiling
Based on the cluster means, the population is divided into four distinct personas:

| Cluster | Persona | Key Characteristics |
| :--- | :--- | :--- |
| **Cluster 0** | **Moderate Families** | Mid-range income (~$39.6k), living with partners, highest number of children (~1.24). |
| **Cluster 1** | **Premium Partners** | High income (~$72.8k), high spending (~$1236), frequent catalog and store shoppers. |
| **Cluster 2** | **Budget Singles** | Lower income (~$36.9k), living alone, high web visits but lowest total spending (~$165). |
| **Cluster 3** | **Elite Singles** | High income (~$70.7k), living alone, highest response rate to campaigns (32%). |

---


# Generating the cluster summary for profiling
cluster_summary = X.groupby("clusters").mean()
print(cluster_summary)
