# E-Commerce Customer Segmentation and Retention Strategy

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Customer segmentation of a UK online retailer using RFM (Recency, Frequency, Monetary) and behavioral features, with K-Means, hierarchical clustering, and DBSCAN compared. The final five-segment model is translated into retention and growth recommendations with explicit, assumption-based revenue scenarios.

## Key Findings

| Segment | Customers | Recency (days) | Orders | Avg spend | Revenue share |
|---|---|---|---|---|---|
| Loyal core | 1,431 | 34 | 7.4 | $1,980 | 65.9% |
| New customers | 1,476 | 47 | 2.0 | $481 | 16.5% |
| Lapsed | 930 | 250 | 1.6 | $316 | 6.8% |
| Occasional bulk buyers | 350 | 92 | 3.3 | $773 | 6.3% |
| Key accounts | 5 | 1 | 136.8 | $38,357 | 4.5% |

- A third of customers generate two thirds of revenue. Retaining the loyal core is the highest priority.
- New customers are the largest segment by count but average only two orders. Converting them into repeat buyers is the largest growth lever: moving 10% of them to loyal-core spend levels would add roughly $220K annually.
- Five wholesale-scale accounts average $38K each; each carries the revenue of about 80 new customers and warrants account management.

Revenue figures are scenario estimates under stated assumptions (see the notebook) and would need validation through controlled experiments.

## Approach

1. **Cleaning.** Removed cancelled and adjustment invoices, rows without `CustomerID`, IQR outliers in quantity and unit price, and duplicate rows.
2. **Feature engineering.** Recency (days before the last invoice date in the data), Frequency (distinct invoices), Monetary (total spend), plus average basket size, average quantity, and customer tenure.
3. **Scaling.** `StandardScaler` so that each feature contributes equally to distance.
4. **Clustering.**
   - K-Means for k = 2 to 10, evaluated with the elbow method and silhouette score. k = 5 had the highest silhouette score (0.305).
   - Hierarchical clustering (Ward linkage) to cross-check the five-cluster structure.
   - DBSCAN, which mainly isolated outliers and did not improve on K-Means.
5. **Profiling.** Cluster means, revenue share, and segment-specific actions.

## Repository Structure

```
├── notebooks/
│   └── customer_segmentation_rfm.ipynb   # Full analysis
├── data/
│   └── README.md                         # Dataset download instructions
├── requirements.txt
└── LICENSE
```

## Getting Started

```bash
git clone https://github.com/Patelparth2109/E-Commerce-Customer-Segmentation-Retention-Strategy.git
cd E-Commerce-Customer-Segmentation-Retention-Strategy
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

Download the dataset as described in [data/README.md](data/README.md), then open `notebooks/customer_segmentation_rfm.ipynb`.

## Tech Stack

Python, pandas, NumPy, scikit-learn (K-Means, DBSCAN, silhouette analysis), SciPy (hierarchical clustering), Matplotlib, Seaborn

## Future Work

- Validate segment strategies with A/B tests, starting with a second-purchase campaign for new customers
- Add predictive customer lifetime value modeling
- Schedule periodic re-segmentation to track customer movement between segments

## License

Released under the [MIT License](LICENSE).

## Author

Parth Patel · [LinkedIn](https://www.linkedin.com/in/parth-patel-03800917a/)

Dataset: Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository.
