![[Distances Used in ML.jpg]]

# Notions of Distance

Knowing when to use which distance measure can help you go from a poor classifier to an accurate model.
  
## Euclidean Distance
The Euclidean distance measures the straight-line distance between two points in space. It is commonly used in clustering and dimensionality reduction algorithms. For example, it can help determine the similarity between items based on their numerical features, making it useful for recommendation systems.  
  
## Cosine Similarity
Cosine similarity measures the angle between two vectors. It is often used in text mining and natural language processing tasks to determine document or word similarity. Cosine similarity is particularly useful for high-dimensional data, where the magnitude of the vectors is less important than their orientation.  
  
## Jaccard Similarity
Jaccard similarity measures the similarity between two sets by calculating the ratio of their intersection to their union. It is widely used in recommendation systems, clustering, and information retrieval. The Jaccard similarity is especially suitable for binary or categorical data, like user preferences or item tags.  
  
## Manhattan Distance
Manhattan distance calculates the distance by summing the absolute differences of coordinates. It is used in clustering algorithms and anomaly detection tasks. Manhattan distance is suitable when movement is restricted to orthogonal axes, like calculating travel distances in a city grid.  
  
## Minkowski Distance
Minkowski distance is a generalized metric that includes both Euclidean and Manhattan distances. It allows tuning the distance measure by adjusting the parameter "p." The choice of p affects the sensitivity to different features, offering customization based on the problem domain.  
  
## Hamming Distance
Hamming distance measures the difference between two strings by counting the positions where corresponding elements differ. It is commonly used in error detection, DNA sequence analysis, and text classification. Hamming distance is effective for comparing binary or categorical data.  
  
## Gower Distance
Gower distance handles mixed data types, including numerical, categorical, and ordinal features. It is used in clustering and similarity analysis for datasets with different data types. Gower distance enables comparison by appropriately normalizing and calculating differences between objects.  
  
## Chebyshev Distance
The Chebyshev distance measures the maximum difference between the corresponding components of two vectors. It is useful for finding anomalies, like detecting unusual pixel values in images.  
  
## Sørensen-Dice Index
The Sørensen-Dice Index measures the similarity between two sets by looking at their overlap. It is commonly used to compare binary or categorical data, like comparing document similarity or clustering similar texts.