# ML_Internship_Week_03
# Documentation of the K-Means Clustering Process

## 1. Introduction
This document outlines the complete process of applying K-means clustering to a dataset, determining the optimal number of clusters, and analyzing the resulting clusters. The goal was to segment customers into distinct groups based on their features, providing insights that could drive business decisions.

## 2. Data Loading and Basic Exploratory Data Analysis (EDA)

### 2.1 Loading the Dataset
I loaded the dataset into a Pandas DataFrame from a CSV file named `customer_data.csv`. This dataset contained various features describing customer attributes.

### 2.2 Exploratory Data Analysis
- **Data Overview:** I used the `info()` method to display the dataset's structure, including the number of entries, data types, and presence of missing values.
- **Statistical Summary:** The `describe()` method provided summary statistics of the numerical features.
- **Data Visualization:** I plotted histograms of key features to understand their distributions.

# Data Preprocessing
## Handling Missing Values
I dropped rows with missing values to ensure data quality.

# Encoding Categorical Variables and Scaling Features
I identified categorical and numerical columns and used a ColumnTransformer to encode categorical variables and scale numerical features.

# Determining the Optimal Number of Clusters
## Elbow Method
I used the Elbow Method to determine the optimal number of clusters. This involved fitting the K-means algorithm with different values of k (number of clusters) and plotting the Sum of Squared Errors (SSE) for each k. The optimal number of clusters is typically at the "elbow point" where the rate of decrease in SSE slows down.

# Decision for the Number of Clusters
Based on the elbow plot, I determined the optimal number of clusters to be 3. This value was chosen because it balanced the trade-off between having too few clusters (high SSE) and too many clusters (increased complexity without significant SSE reduction).

# K-Means Clustering
I applied the K-means algorithm with the optimal number of clusters (k=3). Each customer was assigned to one of the clusters.

# Analysis of Clusters
Cluster Profiling
I analyzed the characteristics of each cluster by calculating the mean values of the numerical features for each cluster. This provided insights into the typical profile of customers within each cluster.

# Visualization of Clusters
I visualized the clusters using scatter plots, allowing for a clear representation of how customers were grouped based on selected feature pairs.

# Conclusion
The K-means clustering process successfully segmented customers into three distinct clusters. These clusters provided valuable insights into customer behavior and preferences, enabling targeted marketing strategies and personalized customer experiences. Further analysis could refine these clusters and explore additional features for more granular segmentation.
