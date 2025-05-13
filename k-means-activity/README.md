# K-Means Clustering Activity

## Overview

This activity involves implementing the K-Means clustering algorithm to analyze the "Penguins" dataset. The dataset contains measurements for three different species of penguins: Adelie, Chinstrap, and Gentoo. The goal is to use clustering techniques to group the penguins based on their physical characteristics.

## Group 2

### Group Members:

| Name                        | Score |
|-----------------------------|-------|
| Jave Anthony Espiritu       | 100   |
| Yuan Haley Enriquez         | 100   |
| James Daniel Esguerra       | 100   |
| Dale Andrew Fajardo         | 100   |
| Marc Daniel Falic           | 100   |
| Emmanuel Joseph Garlando    | 100   |
| China Mae Gonzales          | 100   |
| John Pol Jalapan            | 100   |

## Dataset

The dataset includes the following columns:
- `culmen_length_mm`: Culmen length (mm)
- `culmen_depth_mm`: Culmen depth (mm)
- `flipper_length_mm`: Flipper length (mm)
- `body_mass_g`: Body mass (g)
- `sex`: Penguin sex

## Steps Involved

1. **Data Cleaning**: 
  - Handle missing values by dropping rows with missing data.
  - Remove outliers based on specific conditions for the `flipper_length_mm` feature.

2. **Random Sampling**: 
  - Randomly select 100 data points from the cleaned dataset to make the analysis more manageable.

3. **Feature Selection**: 
  - Select relevant numerical features for clustering: `culmen_length_mm` and `culmen_depth_mm`.

4. **Data Standardization**: 
  - Standardize the features using `StandardScaler` to ensure all features contribute equally to the clustering process.

5. **K-Means Algorithm Implementation**:
  - Initialize centroids by randomly selecting `k` data points.
  - Assign each data point to the nearest centroid.
  - Update centroids by calculating the mean of the data points assigned to each cluster.
  - Check for convergence by comparing old and new centroids.
  - Repeat the process until convergence or the maximum number of iterations is reached.

6. **Elbow Method**:
  - Use the elbow method to determine the optimal number of clusters by plotting the within-cluster sum of squares (WCSS) for each value of `k`.

7. **Visualization**:
  - Visualize the changes of centroids for each iteration of the K-Means algorithm.
  - Animate the clustering process and save the animation as a video file.

## Findings

- The optimal number of clusters was determined using the elbow method. `(k = 2)`
- The K-Means algorithm successfully grouped the penguins into clusters based on their physical characteristics.
- The animation provided a visual representation of how the centroids and clusters evolved over iterations.

## Conclusion

This activity demonstrated the application of the K-Means clustering algorithm on the "Penguins" dataset. By following the steps of data cleaning, feature selection, standardization, and clustering, we were able to group the penguins into meaningful clusters. The elbow method helped in determining the optimal number of clusters, and the visualization provided insights into the clustering process.
>>>>>>> main

