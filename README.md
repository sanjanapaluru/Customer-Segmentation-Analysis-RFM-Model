# 🛍️ Customer Segmentation using RFM Analysis & K-Means Clustering

## 📋 Overview
This project demonstrates customer segmentation using **RFM (Recency, Frequency, Monetary)** analysis combined with **K-means clustering** to identify distinct customer groups based on purchasing behavior. The segmentation enables **targeted marketing strategies** and **personalized customer engagement** to improve retention and maximize customer lifetime value.

---

## 🎯 Business Problem
Businesses need to understand different customer types to:

- Allocate marketing resources efficiently  
- Develop targeted retention strategies  
- Identify high-value customers  
- Personalize customer communications  
- Optimize product offerings  

---

## 📊 Dataset
The analysis uses the **UK Online Retail dataset** containing transactions from **01/12/2010 to 09/12/2011** for a UK-based online retailer that sells unique gifts and homeware.

### Dataset Features:
- `InvoiceNo`: Invoice number (transaction ID)  
- `StockCode`: Product code  
- `Description`: Product description  
- `Quantity`: Quantity purchased  
- `InvoiceDate`: Date and time of transaction  
- `UnitPrice`: Price per unit  
- `CustomerID`: Unique customer identifier  
- `Country`: Customer country  

---

## 🧮 Methodology

### RFM Analysis:
- **Recency (R):** Days since last purchase *(lower is better)*  
- **Frequency (F):** Number of purchases *(higher is better)*  
- **Monetary (M):** Total spending *(higher is better)*  

### Segmentation Approach:
1. **Data Preprocessing**: Cleaned transaction data, calculated total price  
2. **RFM Calculation**: Aggregated customer-level RFM metrics  
3. **RFM Scoring**: Quartile-based scores (1–4) for each RFM dimension  
4. **RFM Segmentation**: Combined scores like `444`, `112`, etc.  
5. **K-Means Clustering**: Unsupervised learning to identify natural clusters  
6. **Segment Analysis**: Interpreted characteristics of each group  

---

## 📈 Results

### Key Customer Segments:
- **Champions (38.7%)**: Frequent, recent, and high-spending  
- **Lost Customers (28.6%)**: Long since last purchase, low frequency  
- **New Customers (12.1%)**: Recent, low-frequency, low spend  
- **At Risk (5.4%)**: Previously good customers, now inactive  
- **Cannot Lose Them (6.1%)**: High-spending but inactive  
- **Needs Attention (4.6%)**: Active but spending less  

### K-Means Clustering:
- **Optimal Clusters**: 3  
- **Cluster 1 (30.5%)**: High-value active customers  
- **Cluster 0 (46.9%)**: Medium-value regular buyers  
- **Cluster 2 (22.6%)**: Inactive/low-value customers  

---

## 📂 Files in this Repository
| File | Description |
|------|-------------|
| `customer_segmentation.ipynb` | Jupyter Notebook with full analysis |
| `data.csv` | Sample transaction data |
| `rfm_customer_segments.csv` | Output file with labeled segments |
| `tableau_dashboard.twbx` | Tableau dashboard for visualization |

---

## 🚀 Implementation Steps

### 1. Data Loading & Exploration
- Load data, inspect structure, handle missing values

### 2. Preprocessing
- Remove returns, invalid data  
- Calculate total spend per invoice

### 3. RFM Analysis
- Set snapshot date  
- Compute Recency, Frequency, Monetary per customer  
- Create RFM scores (quartile ranking)

### 4. Customer Segmentation
- Label customers (e.g., Champions, Lost, New)  
- Analyze segment characteristics  
- Link to business goals (retention, upsell, etc.)

### 5. K-Means Clustering
- Normalize RFM data  
- Use Elbow Method to choose `k`  
- Apply `KMeans` and assign clusters  
- Compare to RFM segments

### 6. Visualization
- **Tableau Dashboard** with:
  - Segment distribution
  - RFM metrics
  - Top customer lists
  - Comparison of clusters

---

## 📊 Tableau Dashboard Features
- **Segment Distribution** Pie Chart  
- **Bar Graphs**: RFM comparison by segment  
- **Customer Table**: Filterable and color-coded  
- **Interactive Filters**: Segment, Cluster, Spending Range  
- **Insights**: Targeted strategies based on segment behavior  

---

## 🔮 Business Recommendations

| Segment | Action |
|---------|--------|
| **Champions** | Reward them, upsell, referral programs |
| **Loyal Customers** | Encourage engagement, early access |
| **Potential Loyalists** | Send offers, convert to loyal |
| **New Customers** | Onboarding, welcome gifts |
| **At Risk** | Re-engagement campaigns |
| **Cannot Lose Them** | Personalized win-back offers |
| **Lost** | Understand churn, offer incentives |

---

## 🛠️ Installation & Usage

### 🔧 Requirements
- Python 3.7+
- pandas, numpy, matplotlib, seaborn
- scikit-learn, plotly (optional)
- Tableau Desktop or Tableau Public

### ▶️ Run Locally
```bash
# Clone the repo
git clone https://github.com/sanjanapaluru/Customer-Segmentation-Analysis-RFM-Model

# Open and run the notebook
jupyter notebook Cluster.ipynb
