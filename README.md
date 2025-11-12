# IRIS-CLASSIFICATION USING SOM

## 1. Introduction

**Self-Organizing Map (SOM)** is a type of Artificial Neural Network (ANN) designed for unsupervised learning. It is primarily used for clustering and visualizing high-dimensional data by projecting it onto a 2D grid.

## 2. What is SOM?

- SOMs group similar data points together without labeled outputs.
- They divide input data into clusters, representing complex multi-dimensional data on a two-dimensional grid for intuitive visualization.

## 3. Core Concepts

- SOMs consist of a grid of neurons, each with an associated weight vector.
- **Training Process:**
  1. Find the Best Matching Unit (BMU) – the neuron whose weight vector is closest to the input vector.
  2. The BMU and its neighboring neurons adjust their weights to resemble the input vector.
  3. Over time, neurons self-organize, resulting in the clustering of similar input data points.

## 4. Mapping Data Points

- Each input data point is compared with all neurons using a distance metric.
- The neuron with the smallest distance is chosen as the BMU.
- The BMU and its neighbors update their weights to move closer to the input data point.
- Nearby neurons represent similar data, preserving topological relationships in the input space.

## 5. Distance Functions

SOMs use functions to measure the distance between a neuron's weight vector and the input vector. Common choices:
- Euclidean Distance
- Manhattan Distance
- Cosine Distance
- Chebyshev Distance

## 6. Neighborhood Function

After identifying the BMU, its neighboring neurons are updated toward the input vector. The neighborhood function determines:
- Which neurons are included in the BMU’s neighborhood.
- The strength of the update for each neighbor.
- Neurons closer to the BMU receive larger updates, preserving the data’s topology.

Common neighborhood functions:
- Gaussian
- Bubble
- Mexican Hat
- Triangle

## 7. Iterative Learning Process

- Learning occurs over multiple dataset iterations.
- **Training Steps:**
  1. Initialize neuron weights (usually random).
  2. For each input vector:
     - Compute the distance to all neurons.
     - Identify the BMU.
     - Update BMU and neighbors’ weights toward the input.
  3. Adjust learning rate and neighborhood radius:
     - Learning rate controls update magnitude.
     - Neighborhood radius sets BMU’s influence range.
  4. Repeat until the SOM stabilizes.

Both learning rate and neighborhood radius decrease over time, allowing for gradual refinement.

## 8. Summary Table

| Concept                 | Description                                    |
|-------------------------|------------------------------------------------|
| Learning Type           | Unsupervised                                   |
| Purpose                 | Clustering and visualization                   |
| Structure               | 2D grid of neurons                             |
| BMU                     | Neuron closest to the input vector             |
| Distance Metrics        | Euclidean, Manhattan, Cosine, Chebyshev        |
| Neighborhood Functions  | Gaussian, Bubble, Mexican Hat, Triangle        |
| Key Parameters          | Learning rate, Neighborhood radius             |

## 9. Next Step: Implementation

Later in this tutorial, we’ll implement SOM training using Python, applying each concept step by step.

## 10. Example Visualization

SOMs map high-dimensional data (e.g., 10+ features) into a 2D grid where similar points cluster together. Use cases include:
- Customer segmentation
- Pattern recognition
- Dimensionality reduction
- Exploratory data analysis

