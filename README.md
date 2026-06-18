# credit-card-segmentation - Internship Project
Credit Card Spending Pattern Segmentation Using K-Means Clustering

# 💳 Credit Card Spending Pattern Segmentation Using K-Means Clustering

## Problem Statement
In 2026, as digital payments dominate India's economy following rapid UPI expansion, banks and fintech companies struggle to personalise offers, detect spending anomalies, and reduce customer churn because they treat all credit card holders identically. This project applies unsupervised machine learning clustering to segment customers by real behavioural spending patterns, enabling data-driven targeted financial strategies.

## Dataset
The dataset was sourced from Kaggle (CC General Dataset) and contains 8,950 credit card customers with 18 behavioural features including balance, purchases, cash advance, credit limit, payments, minimum payments, purchase frequency, and tenure. After data cleaning, 17 features were used for analysis with zero missing values.

## Methodology
The project follows a complete data analytics pipeline. Data was loaded and cleaned by handling 314 missing values using median imputation. Exploratory Data Analysis was performed using distribution plots, correlation heatmaps, and boxplots. Features were scaled using StandardScaler to ensure equal contribution to K-Means distance calculations. The optimal number of clusters was determined using the Elbow Method and Silhouette Score, which both confirmed K=3 as the best choice. K-Means Clustering was then applied and the results were statistically validated using ANOVA.

## Customer Segments Discovered
Three distinct customer segments were identified. Cluster 0 represents Premium Active Spenders with 1,275 customers (14.2%) who have the highest average purchases of $4,187, highest credit limit of $7,642, and a full payment rate of 30% with a low risk score of 18 out of 100. Cluster 1 represents Low Engagement Customers with 6,114 customers (68.3%) who have very low purchases averaging $496 and a full payment rate of 15% with a medium risk score of 52 out of 100. Cluster 2 represents Cash Dependent Risk Customers with 1,561 customers (17.4%) who use cash advance heavily averaging $3,917 with almost zero purchases and a dangerously low full payment rate of only 3%, carrying a high risk score of 87 out of 100.

## Model Validation
The clustering results were validated using two methods. The Silhouette Score of 0.2510 at K=3 was the highest across all tested values of K, confirming that 3 is the optimal number of clusters. ANOVA statistical testing was performed on all 6 key features and all returned F-scores above 200 with p-values of less than 0.001, proving that the differences between clusters are statistically significant and not random.

## Business Recommendations
For Premium Spenders, the bank should offer premium rewards, loyalty programs, proactive credit limit increases, and exclusive travel and lifestyle benefits. For Low Engagement customers, the bank should send personalised cashback offers, gamify spending milestones, and run re-engagement campaigns. For Cash Dependent customers, the bank should monitor for default risk immediately, offer debt restructuring plans, and provide financial wellness counseling.

## Tech Stack
Python was used as the primary programming language with libraries including Pandas and NumPy for data manipulation, Matplotlib and Seaborn for visualizations, Scikit-learn for K-Means clustering, PCA, and StandardScaler, and SciPy for ANOVA statistical testing. Streamlit was used to build an interactive web dashboard and Power BI was used to build a business intelligence report. All development was done in Jupyter Notebook and VS Code.

## How to Run
To run the Jupyter Notebook, open Project-checkpoint.ipynb in Jupyter. To run the Streamlit dashboard, execute streamlit run dashboard.py in the terminal from the project folder.

## Project Structure
The repository contains Project-checkpoint.ipynb which is the complete analysis notebook, dashboard.py which is the Streamlit interactive dashboard, CC GENERAL.csv which is the original Kaggle dataset, credit_card_clusters.csv which is the final clustered dataset with segment labels, powerbi rooman.pbix which is the Power BI dashboard file, and all PNG files which are the charts and visualizations generated during analysis.

## Author
**Preetham Sharvin Danthi**
AI & Machine Learning — 8th Semester
St. Joseph Engineering College, Mangalore (SJEC)
Internship at Rooman Technologies Pvt. Ltd., Bangalore — 2026
