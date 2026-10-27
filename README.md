# Online Retail Analytics: Customer Segmentation, Churn Prediction & Inventory Optimization

### Data-Driven Strategies for E-Commerce Growth

## Project Overview

This project presents an end-to-end analysis of transactional data from a UK-based online retailer to uncover customer purchasing patterns, improve retention strategies, and optimize inventory management.

Using **Python, Exploratory Data Analysis (EDA), Statistical Hypothesis Testing, RFM Analysis, Customer Clustering, and Predictive Machine Learning**, the project transforms raw retail transactions into actionable business insights.

The analysis focuses on identifying high-value customers, predicting customer return behavior, understanding seasonal demand, and exploring opportunities for international market expansion.

## Business Objectives

- Analyze retail sales trends and seasonal purchasing behavior.
- Identify high-value customers using Recency, Frequency, and Monetary (RFM) analysis.
- Segment customers based on purchasing patterns using clustering algorithms.
- Develop machine learning models to predict customer churn and return likelihood.
- Conduct statistical hypothesis testing to validate business assumptions.
- Recommend data-driven strategies for inventory optimization and customer retention.

## Dataset

**Source:** UCI Machine Learning Repository – Online Retail Dataset

**Dataset Overview:**
- Original Transactions: 541,909
- Cleaned Sales Transactions: 392,692
- Unique Customers: 4,338
- Unique Products: 4,070
- Countries Covered: 38
- Time Period: December 2010 – December 2011

The dataset contains invoice numbers, product descriptions, quantities, transaction dates, unit prices, customer IDs, and countries.

**Dataset Link:** https://archive.ics.uci.edu/dataset/352/online+retail

## Technologies & Tools

**Programming Language:** Python

**Data Analysis:** Pandas, NumPy

**Data Visualization:** Matplotlib, Seaborn

**Statistical Analysis:** SciPy, Hypothesis Testing, ANOVA, Chi-Square Tests

**Machine Learning:** Scikit-learn

**Algorithms:** K-Means, Hierarchical Clustering, Gaussian Mixture Models, Logistic Regression, Decision Tree, Random Forest

**Time-Series Analysis:** Statsmodels

**Development Environment:** Jupyter Notebook

## Project Workflow

### 1. Data Cleaning & Preprocessing

- Removed duplicate transactions.
- Handled missing customer identifiers.
- Filtered cancellations, returns, and invalid transaction values for sales analysis.
- Converted transaction dates into appropriate datetime formats.
- Engineered revenue and temporal features for further analysis.

### 2. Exploratory Data Analysis (EDA)

Analyzed customer purchasing behavior, revenue distribution, product performance, geographic sales, and seasonal demand patterns.

Key findings:
- The United Kingdom accounted for approximately 85% of total revenue.
- November and December represented the strongest seasonal sales period.
- International transactions showed higher average values than domestic transactions.
- High-frequency customers generated substantially greater lifetime monetary value.

### 3. RFM Customer Segmentation

Applied Recency, Frequency, and Monetary analysis to classify customers into five actionable segments.

| Customer Segment | Customers | Percentage |
|---|---:|---:|
| Champions | 1,677 | 39% |
| Potential Loyalists | 935 | 22% |
| Hibernating/Lost | 806 | 19% |
| At Risk | 485 | 11% |
| Loyal Customers | 435 | 10% |

This segmentation supports personalized marketing, loyalty programs, and targeted re-engagement campaigns.

### 4. Statistical Hypothesis Testing

Performed five statistical tests to investigate relationships between customer behavior and business performance.

- **Frequency vs Monetary Value:** High-frequency customers generated significantly greater monetary value (p < 0.001).
- **Repeat vs Single-Purchase Customers:** No statistically significant difference in average line-item value (p = 0.499).
- **Weekly Sales Patterns:** Significant differences in transaction amounts across weekdays (p < 0.001).
- **Domestic vs International Sales:** International customers showed significantly higher transaction values (p < 0.001).
- **Country-Level Returns:** Cancellation rates differed significantly across countries (p < 0.001).

Four out of five hypotheses demonstrated statistically significant results.

### 5. Customer Clustering

Implemented and compared three unsupervised learning algorithms to identify natural customer groups.

| Algorithm | Silhouette Score | Davies-Bouldin Index |
|---|---:|---:|
| K-Means | 0.4328 | 0.8925 |
| Hierarchical Clustering | 0.4040 | 0.9405 |
| Gaussian Mixture Model | 0.2855 | 1.0670 |

**Best Performing Algorithm: K-Means (K = 2)**

K-Means provided the strongest cluster separation, identifying broad high-value and low-value customer groups.

### 6. Customer Churn Prediction

Developed supervised machine learning models to predict whether customers would return during a future observation period.

Used a time-based validation approach to reduce data leakage and evaluate model generalization.

**Model Performance:**

| Model | Test Accuracy | ROC-AUC |
|---|---:|---:|
| Logistic Regression | 67.0% | 0.7221 |
| Decision Tree | 65.4% | 0.7109 |
| Random Forest | 65.7% | 0.7219 |

**Selected Model: Logistic Regression**

Logistic Regression achieved the highest test ROC-AUC while offering interpretable results for customer retention decisions.

Important predictive features included:
- Total Customer Spending
- Total Quantity Purchased
- Purchase Recency
- Average Order Value
- Purchase Frequency
- Customer Tenure

## Key Business Insights

**Customer Retention:** High-frequency customers generated approximately 7 times greater monetary value than low-frequency customers, highlighting the importance of loyalty and repeat-purchase strategies.

**Inventory Optimization:** Seasonal sales analysis identified strong holiday demand, supporting proactive stock planning and inventory allocation.

**International Expansion:** International transactions averaged £36.84 compared with £20.86 for UK transactions, indicating opportunities for targeted international growth.

**Predictive Analytics:** Customer return prediction achieved a ROC-AUC of approximately 0.72, demonstrating the potential for data-driven retention targeting.

**Customer Segmentation:** RFM analysis identified 485 at-risk customers who could benefit from personalized re-engagement campaigns.

## Business Recommendations

1. Implement personalized retention campaigns for at-risk customers.
2. Develop VIP loyalty programs for high-value customers.
3. Increase inventory availability ahead of peak holiday demand.
4. Optimize slow-moving product inventory during low-demand periods.
5. Expand targeted marketing efforts in promising international markets.
6. Integrate predictive customer scoring into recurring retention workflows.

## Project Files

```text
online-retail-analytics/
│
├── Final_updated.ipynb
├── Online Retail.xlsx
├── README.md
└── reports/
    └── final_report.docx
```

*Note: The original retail dataset should be downloaded separately if it is not included in the repository.*

## How to Run

1. Clone the repository.
2. Install the required Python packages.
3. Download the Online Retail dataset from the UCI Machine Learning Repository.
4. Place `Online Retail.xlsx` in the working directory.
5. Open `Final_updated.ipynb` in Jupyter Notebook.
6. Run the notebook cells in sequence to reproduce the analysis and visualizations.

**Install dependencies:**

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn statsmodels openpyxl jupyter
```

## Limitations & Future Enhancements

- The dataset covers approximately one year of historical transactions.
- Missing customer identifiers limit the completeness of customer-level analysis.
- Churn prediction performance may vary on newer retail data.
- Business impact estimates are projections rather than measured outcomes.

Future improvements include advanced demand forecasting, customer lifetime value prediction, product recommendation systems, and automated analytics dashboards.

## Project Information

**Course:** DSE 501 – Term Project  
**Institution:** Arizona State University  
**Team:** Team 01  
**Project Date:** December 2025

## Conclusion

This project demonstrates how statistical analysis and machine learning can turn e-commerce transaction data into meaningful business insights. By combining customer segmentation, predictive modeling, hypothesis testing, and seasonal sales analysis, it provides a practical analytical framework for improving customer retention, inventory planning, and strategic decision-making.
