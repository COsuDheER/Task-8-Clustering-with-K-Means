# Task-8-Clustering-with-K-Means

This project focuses on applying K-Means Clustering, a fundamental unsupervised learning algorithm, to segment customers of a mall based on their Annual Income and Spending Score. The goal is to identify distinct customer groups for targeted marketing strategies.

Objective:
Prepare and scale a 2D feature set for clustering.

Use the Elbow Method to systematically determine the optimal number of clusters (K).

Fit the final K-Means model and visualize the resulting customer segments.

Evaluate the quality of the clustering using the Silhouette Score.

Key Steps Performed and Code Highlights:

1. Data Preparation and Scaling:
K-Means is a distance-based algorithm, making feature scaling mandatory.

Features Selected: 'Annual Income (k$)' and 'Spending Score (1-100)'.

Scaling: The selected features were standardized using StandardScaler to ensure all features contribute equally to the distance calculation.

2. Optimal K Determination (The Elbow Method):
To avoid arbitrary selection, the Elbow Method was used to find the most appropriate number of clusters.

Process: The Within-Cluster Sum of Squares (WCSS) (also known as inertia_) was calculated for K ranging from 1 to 10.

Result: The resulting plot clearly showed an "elbow" (a point where the rate of decrease in WCSS slowed significantly) at K=5. This value was chosen for the final segmentation.

3. Final Model Fit and Visualization (K=5):
The final model was trained using K=5 on the scaled data.

Fit: K-Means was fitted to assign a cluster label (0 to 4) to each customer.

Visualization: A scatter plot was created using the original, unscaled income and spending scores for easy interpretation. The customers were color-coded by their assigned cluster, and the five cluster centroids were plotted as large 'X' markers.

4. Clustering Evaluation (Silhouette Score):
The quality of the final segmentation was mathematically validated.

Metric: The Silhouette Score was calculated, measuring the separation distance between the resulting clusters.

Result: A score of 0.5547 was achieved. This is a strong indicator, confirming that the K=5 clusters are well-defined, compact, and sufficiently separated from each other, validating the chosen segmentation.

Conclusion:
This project successfully implemented a robust K-Means clustering solution, identifying five meaningful customer segments that can be used by the mall for highly targeted marketing campaigns and resource allocation (e.g., targeting high-income, high-spending customers vs. low-income, low-spending customers).
