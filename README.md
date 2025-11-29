# Grocery-Store-Customer-Segmentation-Analysis
This project applies unsupervised learning techniques to segment customers based on behavioral, demographic, and transactional data from a marketing campaign. By leveraging Principal Component Analysis (PCA) and clustering algorithms, we uncover distinct customer profiles that inform targeted marketing strategies and business decisions.

# Dataset Summary
- Source: marketing_campaign.csv, it is a tab-separated file
- Size: 2,248 entries, 29 features
## Key Features:
- Demographics: Age, Education, Marital_Status, Income
- Household: Kidhome, Teenhome, Family_size, Is_Parent
- Spending: MntWines, MntMeatProducts, Total_Spent
- Engagement: NumWebPurchases, AcceptedCmp1-5, Response

# Libraries Used
- Data Manipulation - Pandas, Numpy
- Data Visualization - Matplotlib, Seaborn, Yellowbrick
- Machine Learning - scikit-learn (LabelEncoder, StandardScaler, PCA, KMeans, AgglomerativeClustering)
- 3D Plotting - mpl_toolkits.mplot3d

# Methodology
- Data Cleaning: Removed nulls, encoded categorical variables, capped outliers.

##  Feature Engineering:
- Creation of new columns such as Age, Total_Spent, Customer_for, Family_size, Is_Parent
- Simplified Education and Living_With categories
- Scaling: Standardized features for PCA and clustering.
- Dimensionality Reduction: PCA reduced features to 3 components.
### Clustering:
- KMeans with Elbow Method (optimal k = 4)
- Agglomerative Clustering for hierarchical segmentation
- Visualization: 2D and 3D plots, KDEs, boxen plots, swarm plots, joint plots.

 Key Metrics & Visuals
# PCA Summary
| Component | Mean | Std Dev | Min   | Max  |
|----------|------|---------|-------|------|
| col1     | ~0   | 2.81    | -5.94 | 7.49 |
| col2     | ~0   | 1.77    | -4.71 | 6.18 |
| col3     | ~0   | 1.14    | -4.14 | 4.91 |






