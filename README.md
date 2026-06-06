# Customer-Segmentation-Analysis-Using-K-Means-Clustering
# 🛒 Customer Segmentation Analysis Using K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3%2B-orange?style=flat-square&logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

> **Data Analytics Project** — Identifying customer segments using RFM analysis and K-Means Clustering to support targeted marketing strategies.

---

## 📌 Project Overview

This project performs **customer segmentation** on retail transaction data using the **K-Means Clustering** algorithm combined with the **RFM (Recency, Frequency, Monetary)** framework.

The analysis identifies distinct customer groups based on purchasing behavior, enabling data-driven marketing decisions for each segment.

### 🎯 Business Objectives
- Segment customers based on transactional behavior using RFM metrics
- Determine the optimal number of clusters using the Elbow Method and Silhouette Score
- Profile each segment with descriptive statistics and radar charts
- Generate actionable marketing recommendations per segment
- Export clean data for Tableau / Power BI dashboard visualization

---

## 📊 Dataset

| Attribute | Detail |
|-----------|--------|
| Source | Synthetic retail transaction data |
| Records | 1,000 customers |
| Features | CustomerID, LastPurchase, Frequency, TotalSpend, AvgOrderValue |
| RFM Features | Recency (days), Frequency (count), Monetary (IDR) |

> 💡 The dataset is synthetically generated to simulate real-world retail transactions with 4 latent customer types. Replace with your own CSV to apply the same pipeline.

---

## 🔬 Methodology

```
Raw Data
   │
   ▼
Exploratory Data Analysis (EDA)
   │
   ▼
RFM Feature Engineering
   │
   ▼
Log Transform + StandardScaler
   │
   ▼
Optimal K Selection (Elbow + Silhouette)
   │
   ▼
K-Means Clustering (k=4, k-means++)
   │
   ▼
Cluster Evaluation & Profiling
   │
   ▼
Business Insights + Export CSV
```

---

## 🏷️ Customer Segments

| Segment | Recency | Frequency | Monetary | Strategy |
|---------|---------|-----------|----------|----------|
| 🏆 **Champions** | Very recent | Very high | Very high | Loyalty program, VIP perks, early access |
| 💛 **Loyal Customers** | Recent | High | Medium–High | Upsell, cross-sell, personalized offers |
| ⚠️ **At Risk** | Medium | Low | Low–Medium | Re-engagement email, time-limited discounts |
| ❌ **Lost / Inactive** | Very old | Very low | Very low | Last-chance campaign or sunset |

---

## 📈 Results

| Metric | Value |
|--------|-------|
| Algorithm | K-Means (k-means++ init) |
| Optimal K | 4 |
| Silhouette Score | ~0.45–0.55 |
| n_init | 20 |
| Features used | Recency, Frequency, Monetary (log-scaled) |

### Visualizations Generated
| File | Description |
|------|-------------|
| `01_distribution.png` | Feature distributions |
| `02_correlation.png` | Correlation heatmap + scatter |
| `03_rfm_distribution.png` | RFM feature histograms |
| `04_scaling.png` | Before vs after scaling |
| `05_optimal_k.png` | Elbow + Silhouette method |
| `06_silhouette.png` | Silhouette analysis per cluster |
| `07_cluster_viz.png` | PCA 2D projection + scatter |
| `08_radar.png` | Radar profiles per cluster |
| `09_segment_profile.png` | Segment comparison bar charts |
| `10_revenue_by_segment.png` | Revenue contribution by segment |

---

## 🗂️ Repository Structure

```
customer-segmentation-kmeans/
│
├── 📓 customer_segmentation_kmeans.ipynb   ← Main notebook
├── 📄 README.md                            ← This file
├── 📦 requirements.txt                     ← Dependencies
│
├── 📁 output/                              ← Generated after running notebook
│   ├── 01_distribution.png
│   ├── 02_correlation.png
│   ├── ...
│   ├── 10_revenue_by_segment.png
│   └── customer_segments_export.csv        ← Tableau/Power BI ready
```

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/aldisusilo/customer-segmentation-kmeans.git
cd customer-segmentation-kmeans
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook customer_segmentation_kmeans.ipynb
```

### 4. Run all cells
`Kernel` → `Restart & Run All`

> All output plots and the export CSV will be saved automatically in the working directory.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.8+ | Core language |
| Pandas | Data manipulation |
| NumPy | Numerical computing |
| Scikit-Learn | K-Means, PCA, Silhouette |
| Matplotlib | Base plotting |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Interactive development |

---

## 👤 Author

**Surya Aldi Susilo**
Data Science Student — Universitas Pembangunan Nasional Veteran Jawa Timur

[![LinkedIn](https://img.shields.io/badge/LinkedIn-aldisusilo-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/aldisusilo)
[![GitHub](https://img.shields.io/badge/GitHub-aldisusilo-black?style=flat-square&logo=github)](https://github.com/aldisusilo)
[![Tableau](https://img.shields.io/badge/Tableau-Public-E97627?style=flat-square&logo=tableau)](https://public.tableau.com/profile/aldisusilo)

---

## 📄 License

This project is open source under the [MIT License](LICENSE).
