# Mall Customer Segmentation using K-Means Clustering

## Project Overview

This project applies **K-Means Clustering**, an unsupervised machine learning algorithm, to segment mall customers based on their annual income and spending score.

The objective is to identify groups of customers with similar income and spending patterns. These segments can help businesses understand customer behavior and explore more targeted marketing strategies.

## Objectives

- Explore and understand the Mall Customers dataset.
- Select relevant features for customer segmentation.
- Determine a suitable number of clusters using the Elbow Method.
- Train a K-Means clustering model.
- Visualize customer clusters and their centroids.
- Interpret the resulting customer segments.
- Evaluate clustering quality using the Silhouette Score.

## Dataset

**File:** `Mall_Customers.csv`

The dataset contains 200 customer records and five columns:

| Feature | Description |
|---|---|
| CustomerID | Unique customer identifier |
| Gender | Customer gender |
| Age | Customer age |
| Annual Income (k$) | Annual income in thousands of dollars |
| Spending Score (1-100) | Spending score assigned by the mall |

The dataset contains no missing values.

### Selected Features

The model uses two features:

- `Annual Income (k$)`
- `Spending Score (1-100)`

`CustomerID`, `Gender`, and `Age` are excluded from the clustering model.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Jupyter Notebook

## Project Workflow

1. Import the required libraries.
2. Load and inspect the dataset.
3. Check missing values and data types.
4. Select Annual Income and Spending Score.
5. Visualize the relationship between the selected features.
6. Apply the Elbow Method to examine different cluster counts.
7. Train the K-Means model with five clusters.
8. Visualize the clusters and their centroids.
9. Analyze the characteristics of each customer segment.
10. Evaluate clustering quality using the Silhouette Score.

## Algorithm: K-Means Clustering

K-Means is an unsupervised learning algorithm that groups data points into a predefined number of clusters.

The algorithm assigns each customer to a cluster based on distance from cluster centroids and iteratively updates the centroids to reduce within-cluster variation.

The Elbow Method was used to select **K = 5** as a reasonable choice for this dataset.

## Results

| Metric | Result |
|---|---:|
| Total customers | 200 |
| Selected features | 2 |
| Number of clusters | 5 |
| Silhouette Score | 0.5539 |

### Customer Distribution

| Cluster | Number of Customers | Percentage |
|---|---:|---:|
| Cluster 0 | 81 | 40.5% |
| Cluster 1 | 39 | 19.5% |
| Cluster 2 | 22 | 11.0% |
| Cluster 3 | 35 | 17.5% |
| Cluster 4 | 23 | 11.5% |

### Customer Segment Interpretation

| Cluster | Average Annual Income (k$) | Average Spending Score | Interpretation |
|---|---:|---:|---|
| 0 | 55.30 | 49.52 | Average-income, average-spending customers |
| 1 | 86.54 | 82.13 | High-income, high-spending customers |
| 2 | 25.73 | 79.36 | Low-income, high-spending customers |
| 3 | 88.20 | 17.11 | High-income, low-spending customers |
| 4 | 26.30 | 20.91 | Low-income, low-spending customers |

These segments suggest different potential marketing approaches, such as loyalty programs, premium offers, budget-friendly promotions, and personalized recommendations.

## Model Evaluation

The model achieved a **Silhouette Score of 0.5539** for five clusters.

The Silhouette Score ranges from -1 to +1. A positive score of this magnitude suggests that the clusters have a reasonable degree of separation in the selected feature space.

The Elbow Method and Silhouette Score provide useful internal evaluation, but they do not establish that five clusters are universally optimal for every business use case.


## Limitations

- Only Annual Income and Spending Score are used for clustering.
- The number of clusters is selected primarily using the Elbow Method.
- The clustering results depend on feature selection and model initialization.
- The dataset is relatively small, containing 200 customers.
- Customer segments describe patterns in the dataset and do not guarantee future purchasing behavior.

## Future Improvements

- Compare Silhouette Scores across multiple values of K.
- Compare clustering results with and without feature scaling.
- Explore additional clustering algorithms such as Agglomerative Clustering and DBSCAN.
- Analyze age and gender separately to investigate additional customer patterns.
- Evaluate the usefulness of these segments using real marketing outcomes.

## Conclusion

This project demonstrates how unsupervised machine learning can be used to identify customer segments from annual income and spending behavior. K-Means clustering produced five interpretable groups, with a Silhouette Score of 0.5539.

The resulting segments provide a starting point for customer behavior analysis and data-driven marketing exploration.

---

