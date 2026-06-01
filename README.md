# **Mall Customer Segmentation using 3D K-Means Clustering**

## Project Overview
This project focuses on building an **Unsupervised Machine Learning pipeline** to segment a retail mall's customer base. By analyzing behavioral patterns across three core dimensions—**Age, Annual Income, and Spending Score**—the model discovers hidden customer personas without pre-existing target labels. 

The ultimate business goal is to help marketing teams transition from generic broadcasting to highly personalized, high-ROI target campaigns, maximizing customer lifetime value (CLV).

## Tools & Libraries Used
- **Language:** Python
- **Environment:** Jupyter Notebook (Anaconda)
- **Data Manipulation:** Pandas, NumPy
- **Data Preprocessing:** Scikit-Learn (StandardScaler)
- **Machine Learning:** Scikit-Learn (KMeans, silhouette_score)
- **Visualization:** Matplotlib, Seaborn, Plotly (3D Interactive Plots)

## Machine Learning Pipeline
1. **Data Exploration & Cleaning:** Inspected data types, checked for missing values, and dropped unnecessary columns.
2. **Feature Scaling:** Applied `StandardScaler` (Z-Score Standardization) to bring Age, Annual Income, and Spending Score to the same mathematical scale for fair distance calculations.
3. **Hyperparameter Optimization:** Used the **Elbow Method** (plotting WCSS for K=1 to 10) to determine the optimal number of clusters, which was found to be **K = 5**.
4. **Model Training:** Trained the K-Means algorithm using `init='k-means++'` and `random_state=42`.
5. **Statistical Validation:** Evaluated cluster separation using the **Silhouette Score** and cross-tabulated results with **Gender Distribution**.

## Discovered Customer Personas
The model successfully identified 5 distinct behavioral profiles:
- **Cluster 0:** *Sensible Spenders* (Middle-aged, average income & average spend)
- **Cluster 1:** *VIP Stars* (High income & high spend — primary revenue drivers)
- **Cluster 2:** *Carefree Young* (Low income but high spend — trend-driven)
- **Cluster 3:** *Conservative Earners* (High income but low spend — cautious buyers)
- **Cluster 4:** *Budget Shoppers* (Low income & low spend — highly price-sensitive)

## Key Validation Results
- **Silhouette Coefficient:** **0.4085** (Confirms robust mathematical boundaries and healthy cluster separation for 3D behavioral data).
- **Demographic Check:** Cross-tabulation revealed clear gender dominance in specific clusters (e.g., Cluster 0 and 3 are female-dominated), confirming that the mathematical clusters map onto real-world human behavior.

## Real-Time Deployment Simulation
The repository includes a production-ready function (`smart_predict`) that simulates a live Point-of-Sale (POS) integration. When a new customer's Age, Income, and Spend metric are input, the engine instantly scales the data, predicts the cluster category, and triggers a highly tailored marketing action.

## Connect with Me
- **LinkedIn:** www.linkedin.com/in/palwasha-sheikh-0286a71a7
- **Email:** palwashamushtaq123@email.com
