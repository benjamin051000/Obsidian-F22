Lecture 2022-11-03

# Metrics
How do you evaluate clustering results?
- Compare labels with external ones
	- e.g., run K-means and Hierarchical, do they yield the same solutions?
- Check if they match some ground-truth labels

# Internal Criteria
- Silhouette Index
- Rand Index

## Silhouette Index
- Measures compactness of clusters
- Separability between clusters
![[Cluster Validity 2022-11-03 14.55.29.excalidraw]]

$$s = \frac{1}{N} \sum_{i=1}^N \frac{b_i - a_i}{max(a_i, b_i)}, -1 \leq s \leq 1$$
Where
- $a_i$ is the avg distance of point $x_i$ to any other point assigned to the *same* cluster
- $b_i$ is the avg distance of point $x_i$ to any other point assigned to a *different* cluster

## Rand Index
$$R = \frac{a + b}{a+b+c+d}$$
Where
- $a$ is number of pairs of points assigned to same cluster in both A and B (where A and B are clusters)
- $b$ is num pairs of points assigned to a different cluster than both A and B
- $c$ is num pairs assigned to same cluster in A but in different clusters in B
- $d$ is num pairs assigned to same cluster in B but in different clusters in A.
