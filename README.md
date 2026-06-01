# Mall-Customer-Segmentation-Analysis
Beyond Demographics: K-Means clustering cracks the customer spending code.
# Mall Customer Segmentation Analysis

> **Customer Clustering & Business Intelligence | K-Means Segmentation | Retail Analytics**

A data science project that segments mall customers into 5 actionable business profiles using K-Means clustering, with comprehensive business recommendations and strategic insights.

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Customer Segments](#customer-segments)
- [Business Recommendations](#business-recommendations)
- [Results & Insights](#results--insights)
- [Technologies](#technologies)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Future Work](#future-work)
- [Author](#author)

---

## 📊 Project Overview

This project applies **unsupervised machine learning** (K-Means clustering) to segment mall customers based on demographic and behavioral features. The analysis bridges the gap between technical data science and actionable business strategy, providing clear segmentation profiles and strategic recommendations for retail operations.

**Key Achievement**: Identified 5 distinct customer personas with non-linear spending patterns, revealing that **income alone does not predict spending behavior**.

---

## 🎯 Business Problem

Mall management needs to understand their customer base to:
- Optimize **tenant mix and floor space allocation**
- Design **targeted marketing campaigns**
- Improve **customer experience and retention**
- Identify **high-value segments and growth opportunities**

Traditional demographic analysis (age, income) fails to explain spending behavior. This project uses clustering to reveal the hidden patterns driving customer value.

---

## 📁 Dataset

| Feature | Type | Range | Notes |
|---------|------|-------|-------|
| **Age** | Numeric | 18-70 years | Customer age |
| **Annual Income** | Numeric | 15k - 137k GHS | Annual household income |
| **Spending Score** | Numeric | 1-100 | Propensity to spend (derived from behavior) |
| **Customer ID** | Categorical | Unique identifier | |

**Dataset Size**: 200 customers | **No missing values**

---

## 🔬 Methodology

### 1. **Data Exploration & Preprocessing**
- Descriptive statistics and distribution analysis
- Feature scaling (StandardScaler) for distance-based algorithms
- Outlier detection and validation

### 2. **Clustering Algorithm: K-Means**
- **Optimal clusters determination**: Elbow method & Silhouette analysis
- **Number of clusters selected**: 5 (balance between granularity and business interpretability)
- **Distance metric**: Euclidean distance
- **Initialization**: K-means++ for stable convergence

### 3. **Cluster Profiling**
- Calculate cluster centroids (mean age, income, spending)
- Derive business characteristics for each segment
- Validate segment distinctness and business relevance

### 4. **Business Translation**
- Map technical metrics to business language
- Develop actionable recommendations per segment
- Design strategic implications (tenant mix, marketing, experience)

---

## 🎯 Key Findings

### 🔴 **Income ≠ Spending** (Non-Linear Relationship)

The strongest insight: **High income does not guarantee high spending.**

| Cluster | Income | Spending | Ratio |
|---------|--------|----------|-------|
| Cluster 2 (Affluent Prof.) | 86.1k | 81.5 | 1.00× (baseline) |
| **Cluster 3 (Young Enthusiasts)** | **26.1k** | **74.8** | **2.87×** (spend 3× their income ratio) |
| Cluster 4 (Practical Youth) | 54.3k | 40.9 | 0.75× |
| Cluster 1 (Steady Retirees) | 47.6k | 41.7 | 0.88× |
| **Cluster 5 (Selective Splurgers)** | **89.8k** | **18.5** | **0.21×** (spend 1/5 of income ratio) |

**Implication**: Motivation, lifestyle, and values drive spending—not ability to pay.

---

## 👥 Customer Segments

### **Cluster 1: Steady Retirees** (32% of base)
```
Age: 55 | Income: 47.6k GHS | Spending: 41.7/100
```
- **Profile**: Older, modest income, budget-conscious
- **Motivation**: Value, practicality, stability
- **Actions**: Discount retailers, accessibility, essentials
- **Strategic Focus**: Retention & comfort

### **Cluster 2: Affluent Professionals** ⭐ (22% of base)
```
Age: 33 | Income: 86.1k GHS | Spending: 81.5/100 [HIGHEST]
```
- **Profile**: Young, high earners, high spenders (revenue hero)
- **Motivation**: Quality, status, premium experience
- **Actions**: Luxury brands, VIP services, personalization
- **Strategic Focus**: Revenue maximization & VIP experience

### **Cluster 3: Young Enthusiasts** 🔥 (14% of base)
```
Age: 26 | Income: 26.1k GHS | Spending: 74.8/100
```
- **Profile**: Youngest, lowest income, aspirational spending
- **Motivation**: Trends, social status, peer influence
- **Actions**: Fast fashion, social media, affordable luxury
- **Strategic Focus**: Engagement & loyalty (manage over-extension risk)

### **Cluster 4: Practical Young Professionals** (25% of base)
```
Age: 27 | Income: 54.3k GHS | Spending: 40.9/100
```
- **Profile**: Young, moderate income, value-conscious
- **Motivation**: Quality at fair price, convenience
- **Actions**: Mid-range retail, deals, F&B mix
- **Strategic Focus**: Frequency & cross-promotion

### **Cluster 5: Selective Splurgers** (17% of base)
```
Age: 44 | Income: 89.8k GHS | Spending: 18.5/100 [LOWEST]
```
- **Profile**: Highest earners, lowest spenders (mystery segment)
- **Motivation**: Quality, efficiency, niche offerings
- **Actions**: Specialty stores, curated experience, personalization
- **Strategic Focus**: Investigate & unlock potential

---

## 💡 Business Recommendations

### **Immediate Actions** (0-3 months)

1. **Maximize Cluster 2** (Affluent Professionals)
   - Launch VIP lounge & priority services
   - Curate premium tenant mix
   - Implement personalized marketing

2. **Investigate Cluster 5** (Selective Splurgers)
   - Survey to understand spending barriers
   - Test niche retailers & specialty stores
   - Unlock revenue potential from high earners

3. **Engage Cluster 3** (Young Enthusiasts)
   - Launch influencer & social media campaigns
   - Create Instagram-worthy spaces
   - Implement loyalty program (financial responsibility)

### **Medium-Term Strategy** (3-12 months)

| Goal | Action | Expected Impact |
|------|--------|-----------------|
| Revenue Growth | Unlock Cluster 5 potential | +10-15% from segment |
| Frequency | Increase Cluster 4 visits | +20% visit frequency |
| Risk Management | Monitor Cluster 3 over-extension | Reduce churn; build loyalty |
| Retention | Invest in Cluster 1 comfort | 90%+ retention rate |

### **Tenant Mix Optimization**

- **Premium Zone** (Cluster 2): Luxury fashion, jewelry, fine dining
- **Trendy Zone** (Cluster 3): Fast fashion, beauty, affordable luxury
- **Value Zone** (Clusters 1, 4): Mid-range retail, grocery, casual dining
- **Specialty Zone** (Cluster 5): Niche stores, wellness, premium groceries

---

## 📈 Results & Insights

### Cluster Characteristics Summary

```
┌─────────────┬──────┬────────────┬──────────┬──────────────┐
│ Cluster     │ Size │ Age (avg)  │ Income   │ Spending     │
├─────────────┼──────┼────────────┼──────────┼──────────────┤
│ 1 (Retirees)│ 58   │ 55.3       │ 47.6k    │ 41.7 ░░░░░░ │
│ 2 (Affluent)│ 40   │ 32.9       │ 86.1k    │ 81.5 ████████│
│ 3 (Youth)   │ 26   │ 25.8       │ 26.1k    │ 74.8 ███████ │
│ 4 (Practical)│45   │ 26.7       │ 54.3k    │ 40.9 ░░░░░░  │
│ 5 (Selective)│31   │ 44.4       │ 89.8k    │ 18.5 ░░░░    │
└─────────────┴──────┴────────────┴──────────┴──────────────┘
```

### Strategic Segmentation by Age

- **Younger (25-33)**: 63% of base | High engagement | Trend-responsive
- **Older (44-55)**: 37% of base | Value-focused | Stability-seeking

### Revenue Drivers

1. **Cluster 2**: Highest spend per customer (81.5/100) + solid size (22%)
2. **Cluster 3**: High engagement despite low income (growth potential)
3. **Cluster 4**: Largest growth segment if frequency increases (25% of base)

### Risk Factors

- **Cluster 3**: Over-extension risk (spending 3× their income ratio)
- **Cluster 5**: Untapped potential (high income, minimal spending)

---

## 🛠 Technologies

**Data Analysis & ML:**
- Python 3.8+
- pandas — Data manipulation
- scikit-learn — K-Means clustering, preprocessing
- NumPy — Numerical computing
- Matplotlib & Seaborn — Visualization

**Optional Tools:**
- Jupyter Notebook — Exploration & analysis
- SQL — For data extraction (if sourced from database)

---

## 🚀 Usage

### Prerequisites
```bash
pip install pandas scikit-learn numpy matplotlib seaborn
```

### Running the Analysis
```bash
# Load data and perform clustering
python clustering_analysis.py

# Generate cluster profiles
python profile_clusters.py

# Create visualizations
python visualize_segments.py
```

### Expected Output
- `cluster_profiles.csv` — Segment characteristics
- `business_recommendations.md` — Strategic insights
- `visualizations/` — Charts and diagrams

---

## 📂 Project Structure

```
mall-customer-segmentation/
│
├── README.md                          # This file
├── business_segmentation.md           # Full business analysis
│
├── data/
│   └── mall_customers.csv             # Raw customer data (200 rows)
│
├── notebooks/
│   ├── 01_exploratory_analysis.ipynb  # EDA & data profiling
│   ├── 02_clustering_model.ipynb      # K-Means implementation
│   └── 03_business_insights.ipynb     # Segment profiling & translation
│
├── scripts/
│   ├── data_preprocessing.py          # Data cleaning & scaling
│   ├── kmeans_clustering.py           # Clustering algorithm
│   ├── profile_clusters.py            # Segment characterization
│   └── visualize_segments.py          # Charts & dashboards
│
├── outputs/
│   ├── cluster_profiles.csv           # Cluster centroids & stats
│   ├── customer_segments.csv          # Labeled customers by cluster
│   └── visualizations/                # PNG charts
│
└── requirements.txt                   # Dependencies
```

---

## 🔮 Future Work

### Model Enhancements
- [ ] Test alternative clustering algorithms (DBSCAN, Hierarchical)
- [ ] Incorporate additional features (purchase history, category preferences)
- [ ] Temporal analysis (seasonal patterns, churn trends)
- [ ] Customer lifetime value (CLV) modeling

### Business Extensions
- [ ] RFM segmentation (Recency, Frequency, Monetary)
- [ ] Predictive churn modeling for at-risk segments
- [ ] A/B testing on segment-specific marketing campaigns
- [ ] Personalization engine for Cluster 2 & 5
- [ ] Loyalty program design by segment

### Analytics Pipeline
- [ ] Real-time clustering dashboard (Power BI / Tableau)
- [ ] Automated cluster re-training (monthly/quarterly)
- [ ] Integration with CRM system for segment-based operations
- [ ] SQL queries for segment filtering and analysis

---

## 📊 Key Metrics to Track

**Segment Performance:**
- Visit frequency by segment
- Average spend per visit (basket size)
- Customer lifetime value (CLV) by segment
- Churn rate by segment
- Net Promoter Score (NPS) by segment

**Business KPIs:**
- Revenue contribution by segment (%)
- Tenant sales by segment
- Marketing ROI by segment
- Footfall by demographic
- Year-over-year growth by segment

---

## 🤝 Contributing

Feedback and improvements welcome! Areas for contribution:
- Additional feature engineering
- Advanced clustering techniques
- Real-time segmentation pipeline
- Interactive visualizations
- Case studies from other retail domains

---

## 📝 License

This project is open source and available under the MIT License.

---

## 👤 Author

**Priscilla Naadu Lartey**  
Data Scientist | Big Data Analytics | AI/ML Engineering  
📧 [LinkedIn](https://linkedin.com) | 🐙 [GitHub](https://github.com/PriscillaLartey)

---

## 📚 References & Resources

- [K-Means Clustering - Scikit-Learn](https://scikit-learn.org/stable/modules/clustering.html#k-means)
- [Elbow Method for Optimal Clusters](https://en.wikipedia.org/wiki/Elbow_method_(clustering))
- [Silhouette Analysis](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html)
- [Customer Segmentation Best Practices](https://en.wikipedia.org/wiki/Market_segmentation)

---

## 💬 Questions?

Feel free to open an issue or reach out with questions about:
- Clustering methodology
- Business interpretation
- Extending the analysis
- Integration into your systems

---

**Last Updated**: 1st June 2026  
**Dataset Size**: 200 customers | **Clusters**: 5 | **Features**: 3 (Age, Income, Spending Score)
