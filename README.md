# Marketing Campaign Analysis

This project explores customer behaviour, spending patterns, and marketing campaign effectiveness using advanced analytics and machine learning. The goal is to identify high‑value customer segments, predict campaign response, and provide actionable insights to improve marketing ROI.

The dataset includes 2,213 customers, 29 features, and 5 marketing campaigns, enabling a full lifecycle analysis from data cleaning to modelling and strategic recommendations.

## Methodology

- **RFM segmentation** — quintile-ranked Recency/Frequency/Monetary scoring to classify customers into behavioural segments (Champions, At Risk, Lost/Inactive, etc.)
- **K-Means clustering** — unsupervised segmentation with elbow-method and silhouette-score validation to select the optimal number of clusters, visualised via PCA
- **Random Forest classification** — predicts campaign response with cross-validated ROC-AUC, feature importance, and a full classification report
- **Customer Lifetime Value (CLV) estimation** — historical CLV by RFM segment, used to set acquisition budget guidelines
- **Campaign ROI analysis** — response rate and ROI per campaign against actual contact cost and revenue-per-response figures
- **Statistical testing** — Welch's t-test to validate whether child-free households spend significantly more

## Results

- Random Forest: **Test ROC-AUC ≈ 0.87** (5-fold CV ≈ 0.89 ± 0.03)
- Income is the strongest predictor of spend (Pearson r ≈ 0.79)
- Top 20% of customers by spend generate the majority of revenue (Pareto concentration)
- Full findings, segment-specific recommendations, and a prioritised action plan are in the notebook's Executive Summary section

## Tech Stack

Python, pandas, NumPy, scikit-learn, seaborn, matplotlib, SciPy

## How to Run

```
pip install pandas numpy scikit-learn seaborn matplotlib scipy
```
Open `Marketing.ipynb` in Jupyter and run all cells top to bottom (`marketing_campaign.csv` is included in this repo).

## Author

Tateyama Orpa
