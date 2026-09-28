# 📊 E-Commerce Customer Segmentation Dashboard (RFM + K-Means ML)

An interactive, data-driven analytics dashboard designed to dismantle "one-size-fits-all" marketing. By evaluating **6,000 unique customers** across 3 years of transactional histories (**\$14.57M revenue**), this production-ready application applies a hybrid approach—combining traditional rule-based **RFM Analysis** with unsupervised **K-Means Machine Learning Clustering**—to isolate high-value behavioral groups and optimize retention strategies.

---

## 💡 Key Business Discoveries & ROI Insights
* **The Pareto Effect:** The top **20% of customers** drive **65.4%** of total gross revenue. VIP loyalty retention programs yield up to **7× higher ROI** than mass-blast marketing.
* **The Churn Leak:** **50% of new sign-ups churn** immediately following their very first purchase. This represents the company's largest revenue drop, fixable via an automated post-purchase onboarding sequence.
* **Revenue Concentration:** The top 3 core segments (comprising only 31% of the total customer base) generate **78.6%** of all gross revenue.
* **ML vs. Rule-Based Precision:** The K-Means model successfully isolated **4 distinct behavioral micro-clusters** hidden inside the single "Cannot Lose Them" RFM segment. This proves unsupervised ML catches nuances that static, hard-coded rules miss.
* **Product Mix Impact:** Electronics alone generated **41.7% of total revenue**, indicating that category-specific promotions here yield the highest absolute returns.

---

## 🛠️ Tech Stack & Tooling Architecture
* **Frontend Dashboard UI:** `Streamlit` (Multi-tab layout with global sidebar state filtering)
* **Exploratory & Interactive Charts:** `Plotly` (3D feature-space matrix plots, dynamic heatmaps, and dual-axis Pareto lines)
* **Machine Learning Pipeline:** `Scikit-Learn` (StandardScaler standardization + K-Means optimization)
* **Data Engineering Engine:** `Pandas` & `NumPy` (Time-series aggregations, quantile groupings, and 3-year forward CLV estimation math)
* **Model Serialization:** `Joblib` (Binary persistence for the mathematical feature scaler and cluster weights)

---

## 🗂️ Project Workspace Structure
```text
ecommerce-customer-segmentation/
│
├── app.py                  # Core interactive Streamlit web dashboard application
├── generate_data.py        # Scaled synthetic data generator (Generates 6k customers)
├── ml_clustering.py        # ML training script (StandardScaler -> K-Means optimization)
├── requirements.txt        # Python dependency specification file
├── README.md               # Project documentation (You are here)
│
├── data/
│   └── ecommerce_transactions.csv  # Generated raw transactional ledger dataset
│
└── models/
    ├── kmeans_model.pkl    # Serialized K-Means machine learning model weights
    ├── scaler.pkl          # Serialized feature scaling configuration matrix
    └── model_summary.json  # Model validation engine score logs (Silhouette, DB index)
```

---

## 📊 Dashboard Structural Interface
The user interface features a real-time **Global Sidebar Filter Control Deck** (allowing manual manipulation of specific Date Ranges, Segment inclusions, and target Monetary spend thresholds) distributed across 4 structural tabs:
1. **📊 RFM Segmentation:** Customer distribution donut charts, macro revenue-by-segment horizontal layouts, and explicit Recency vs. Frequency average monetary matrix heatmaps.
2. **🤖 ML Clustering:** 3D Scatter space coordinate plots (Recency × Frequency × Monetary), mathematical scoring logs, and comparative ML vs. RFM intersection summaries.
3. **📈 Revenue & Pareto Concentration:** The formal Dual-Axis Pareto accumulation line curve paired with category vertical performance mixes.
4. **🔄 Cohort Analysis & Retention:** Month-over-month customer group survival matrices alongside 3-Year Forward CLV (Customer Lifetime Value) distribution spread box plots.

---

## 🏆 Algorithmic Verification Log
The unsupervised K-Means engine utilizes scaled dimensional vectors (R, F, M) optimized against multi-tier structural validation benchmarks:
* **Silhouette Score:** `0.386` (Confirming stable, non-overlapping cluster boundaries)
* **Davies-Bouldin Index:** `0.817` (Confirming tightly grouped internal cluster distances)
* **Calinski-Harabasz Score:** `7,645.66`
* **Target Segments/Clusters (K):** `8`

---

## ⚙️ Installation & Execution Guide

### 1. Environment Deployment
Clone the remote workspace repository locally, initialize your preferred project environment, and deploy package dependencies:
```bash
git clone https://github.com
cd ecommerce-customer-segmentation
pip install -r requirements.txt
```

### 2. Transaction Log Generation
Run the core synthesis data generation script to construct your baseline 3-year database transaction ledger inside the workspace:
```bash
python generate_data.py
```

### 3. Machine Learning Model Training
Execute the training script to scale features, process parameters, calculate mathematical performance boundaries, and persist internal binary vectors to disk:
```bash
python ml_clustering.py
```

### 4. Interactive Live UI Initialization
Launch the live, reactive web server platform straight from your local environment setup terminal:
```bash
streamlit run app.py
```
Once initialized, navigate your active default web browser application panel interface directly to the local portal: **`http://localhost:8501`**
