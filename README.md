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

# Key Metrics & Visuals
## PCA Summary
| Component | Mean | Std Dev | Min   | Max  |
|----------|------|---------|-------|------|
| col1     | ~0   | 2.81    | -5.94 | 7.49 |
| col2     | ~0   | 1.77    | -4.71 | 6.18 |
| col3     | ~0   | 1.14    | -4.14 | 4.91 |

## Elbow Method
- Optimal clusters: 4
- Distortion score at k=4: 8731.36

## Cluster Distribution
- Cluster 0: Low spenders, minimal engagement
- Cluster 1: Moderate spenders, responsive to promotions
- Cluster 2: High spenders, frequent deal purchasers
- Cluster 3: Wealthy but disengaged, low promo acceptance

### Visuals Used
- 3D Scatter Plot: PCA components colored by cluster
- Countplot: Cluster distribution
- Swarm Plot: Spending behavior across clusters
- Boxen Plot: Number of deals purchased
- KDE & Joint Plots: Spending vs. Age, Education, Family size, etc.
- Contour Plots: Density of spending across demographic variables


# Cluster Insights
## Cluster 0 – Budget-Conscious Singles
- Low income and spending
- Small households, often living alone
- Least responsive to campaigns
## Cluster 1 – Engaged Middle-Class Families
- Moderate income and spending
- Parents with 1–2 children
- Accept promotions and engage with multiple channels
## Cluster 2 – Premium Buyers
- High spenders across all product categories
- Frequent deal and catalog purchases
- Strong digital engagement
## Cluster 3 – Affluent but Passive
- High income, low campaign response
- Minimal purchases despite capacity
- Prefer offline or non-promotional channels


# Marketing Campaign Recommendation
- Use the behavioral and demographic profiles of each cluster to tailor campaigns
## Cluster 0 (Budget-Conscious Singles):
- Offer low-cost bundles and loyalty discounts
- Use SMS or email for direct, low-friction engagement
- Highlight value and savings in messaging
## Cluster 1 (Engaged Middle-Class Families):
- Promote family-oriented packages and seasonal deals
- Use multi-channel campaigns (email, social media, catalogs)
- Incentivize referrals and repeat purchases
## Cluster 2 (Premium Buyers):
- Launch exclusive VIP programs and early-access offers
- Focus on quality, prestige, and convenience
- Use personalized product recommendations and high-touch service
## Cluster 3 (Affluent but Passive):
- Re-engagement campaigns with premium incentives
- Highlight brand values, sustainability, or lifestyle alignment
- Use offline channels and curated experiences to build trust












