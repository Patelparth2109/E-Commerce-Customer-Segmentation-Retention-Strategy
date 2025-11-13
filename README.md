# 🛍️ E-Commerce Customer Segmentation & Retention Strategy

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

A data-driven customer segmentation project using **RFM (Recency, Frequency, Monetary) analysis** and **unsupervised machine learning** to identify high-value customer groups, optimize marketing spend, and drive revenue growth.

---

## 📊 Project Overview

This project addresses key business challenges faced by online retail companies:
- **Declining customer retention rates**
- **Inefficient marketing budget allocation**
- **Inability to identify high-value customer segments**
- **Lack of personalized customer experiences**

By leveraging K-Means clustering on RFM metrics, this analysis segments customers into distinct behavioral groups, enabling targeted retention strategies and data-driven business decisions.

---

## 💼 Business Impact

### Key Results
- **66% of revenue** comes from a single high-value cluster (Cluster 4)
- Identified **VIP customers** with $38K average spend requiring dedicated management
- **Potential annual revenue gain: $550K–$600K** (8-10% uplift) through targeted strategies
- **80/20 dynamic confirmed**: Top 30% of customers drive nearly 80% of revenue

### Strategic Opportunities

| Strategy | Target Segment | Est. Revenue Gain | Growth Potential |
|----------|----------------|-------------------|------------------|
| **Retain Top Buyers** | Cluster 4 | +$150K | +5% retention → +$150K revenue |
| **Upsell Mid-Tier** | Cluster 3 | +$90K | 10-15% conversion to high-spend |
| **Reactivate Dormant** | Clusters 0 & 1 | +$220K | $100 uplift per customer |
| **Protect VIPs** | Cluster 2 | +$100K | Dedicated account management |
| **Total Potential** | — | **$550K–$600K** | **8-10% overall uplift** |

---

## 🎯 Key Features

- **RFM Analysis**: Recency, Frequency, and Monetary value metrics for customer behavior
- **Multiple Clustering Algorithms**: K-Means, Hierarchical Clustering, DBSCAN
- **Elbow Method**: Optimal cluster determination using inertia analysis
- **Business Insights**: Revenue share analysis and actionable recommendations
- **Data Visualization**: Comprehensive charts and cluster distributions
- **Financial Modeling**: Quantified business impact and ROI projections

---

## 📁 Project Structure

```
├── Clustering__1_.ipynb          # Main analysis notebook
├── README.md                      # Project documentation
├── requirements.txt               # Python dependencies
├── .gitignore                     # Git ignore file
├── LICENSE                        # MIT License
└── data/                          # Data directory (not included)
    └── online_retail.xlsx         # Original dataset
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Basic understanding of clustering algorithms and data analysis

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/customer-segmentation.git
   cd customer-segmentation
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the dataset**
   - Dataset: [UCI Machine Learning Repository - Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
   - Place the `online_retail.xlsx` file in the `data/` directory

5. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook Clustering__1_.ipynb
   ```

---

## 📚 Methodology

### 1. Data Preprocessing
- Handled missing values in `CustomerID` field
- Removed cancelled transactions (negative quantities)
- Created total purchase amount feature
- Filtered dataset to relevant date range (2010-2011)

### 2. RFM Feature Engineering
- **Recency**: Days since last purchase (from reference date: Dec 31, 2011)
- **Frequency**: Total number of transactions per customer
- **Monetary**: Total revenue generated per customer

### 3. Data Scaling
- Applied `StandardScaler` for feature normalization
- Ensures equal weight to all RFM dimensions in clustering

### 4. Clustering Analysis
- **K-Means**: Primary algorithm with 5 optimal clusters (Elbow Method)
- **Hierarchical Clustering**: Dendrogram analysis for cluster validation
- **DBSCAN**: Density-based outlier detection

### 5. Business Intelligence
- Revenue share calculation by cluster
- Customer behavior profiling
- Strategic action recommendations per segment

---

## 📈 Technologies Used

- **Python 3.12**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn**: Machine learning algorithms (K-Means, DBSCAN, StandardScaler)
- **SciPy**: Hierarchical clustering and dendrogram visualization
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter Notebook**: Interactive development environment

---

## 🔍 Key Insights

### Cluster Profiles

**Cluster 4 - Core Profit Drivers (66% revenue)**
- Largest customer segment
- Moderate-to-high frequency and monetary value
- **Action**: Implement loyalty programs, exclusive launches, personalized upsells

**Cluster 3 - Mid-Tier Growth Potential (17% revenue)**
- Medium frequency and spending
- High ROI opportunity for upselling
- **Action**: Targeted email campaigns, product bundles, cross-category promotions

**Cluster 2 - VIP/Enterprise Clients (<1% of customers, extremely high value)**
- Average spend: $38K per customer
- Critical for revenue stability
- **Action**: Dedicated account management, concierge service, long-term contracts

**Clusters 0 & 1 - Dormant/Low Engagement (13% revenue)**
- Low frequency and monetary value
- ~2,200 customers with reactivation potential
- **Action**: Win-back campaigns, referral bonuses, personalized discounts

---

## 📊 Sample Visualizations

The notebook includes:
- Elbow curve for optimal cluster selection
- Revenue distribution by cluster (bar charts)
- RFM score distributions
- Cluster characteristics heatmaps
- Customer count per segment

---

## 🎓 Learning Outcomes

This project demonstrates proficiency in:
- **Unsupervised Machine Learning**: K-Means, Hierarchical, DBSCAN clustering
- **Feature Engineering**: RFM metric calculation and business logic
- **Data Preprocessing**: Handling missing data, outliers, and scaling
- **Business Analytics**: Translating ML results into actionable insights
- **Financial Modeling**: Revenue forecasting and ROI estimation
- **Data Visualization**: Creating compelling business intelligence dashboards

---

## 🛠️ Future Enhancements

- [ ] Deploy interactive dashboard using Streamlit or Dash
- [ ] Implement automated customer scoring API
- [ ] Add time-series analysis for churn prediction
- [ ] Integrate predictive CLV (Customer Lifetime Value) modeling
- [ ] Build recommendation engine for personalized marketing
- [ ] Add A/B testing framework for strategy validation

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Parth Patel**
- 🎓 MS in Data Analytics & Information Systems (Applied AI) - Texas State University
- 💼 Former Senior Financial Advisor at Scotiabank
- 🔗 [LinkedIn](https://www.linkedin.com/in/yourprofile)
- 📧 [Email](mailto:your.email@example.com)
- 🌐 [Portfolio](https://yourportfolio.com)

---

## 🙏 Acknowledgments

- Dataset provided by [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php)
- Inspired by real-world e-commerce retention challenges
- Built as part of a comprehensive data science portfolio

---

## 📞 Contact

For questions, feedback, or collaboration opportunities:
- Open an issue on GitHub
- Connect with me on LinkedIn
- Email: your.email@example.com

---

**⭐ If you found this project helpful, please consider giving it a star!**
