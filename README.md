# IRIS-CLASSIFICATION USING SOM

🧠 Self-Organizing Maps (SOM)

Self-Organizing Map (SOM) is a type of Artificial Neural Network (ANN) designed for unsupervised learning.
It is primarily used for clustering and visualizing high-dimensional data by projecting it into a 2D grid.

📘 What is SOM?

SOMs are neural networks that learn to group similar data points together without labeled outputs.
Given a set of input data, the SOM divides it into clusters and represents complex multi-dimensional data on a two-dimensional grid, making visualization easier and intuitive.

🧩 Core Concept

SOMs consist of a grid of neurons, where each neuron has an associated weight vector.
During training:

The neuron whose weight vector is closest to the input vector is identified as the Best Matching Unit (BMU).

The BMU and its neighboring neurons adjust their weights to become more like the input vector.

Over time, this process causes the neurons to self-organize, resulting in clustering of similar input data points.

🗺️ Mapping Data Points

Each input data point is compared with all neurons using a distance metric.

The neuron with the smallest distance is chosen as the BMU.

The BMU and its neighbors update their weights to move closer to the input data point.

This ensures that nearby neurons represent similar data, preserving the topological relationships in the input space.

📏 Distance Functions

SOMs use distance functions to measure how far a neuron’s weight vector is from the input vector.

Commonly used functions:

Euclidean Distance

Manhattan Distance

Cosine Distance

Chebyshev Distance

🌐 Neighborhood Function

After identifying the BMU, its neighboring neurons are updated in the direction of the input vector.
The neighborhood function determines:

Which neurons are considered part of the BMU’s neighborhood.

How strongly each neighboring neuron’s weights are updated.

Neurons closer to the BMU receive larger updates than those farther away, preserving the topological structure of the data.

Common Neighborhood Functions:

Gaussian

Bubble

Mexican Hat

Triangle

🔁 Iterative Learning Process

The SOM learns through multiple iterations over the dataset.

Training Steps:

Initialize all neuron weights (typically random).

For each input vector:

Compute the distance between the input and all neurons.

Identify the BMU (neuron with the smallest distance).

Update the weights of the BMU and its neighbors toward the input vector.

Adjust learning parameters:

The learning rate controls the magnitude of weight updates.

The neighborhood radius determines how far the BMU’s influence extends.

Repeat for many iterations until the SOM stabilizes.

Both the learning rate and neighborhood radius typically decrease over time, allowing the SOM to fine-tune the map structure gradually.

💻 Summary
Concept	Description
Learning Type	Unsupervised
Purpose	Clustering and visualization
Structure	2D grid of neurons
BMU	Neuron closest to the input vector
Distance Metrics	Euclidean, Manhattan, Cosine, Chebyshev
Neighborhood Functions	Gaussian, Bubble, Mexican Hat, Triangle
Key Parameters	Learning rate, Neighborhood radius
🧮 Next Step: Implementation

Later in this tutorial, we’ll implement the iterative training process of SOM using Python, applying the concepts above step by step.

✨ Example Visualization

SOMs can map high-dimensional data (e.g., 10+ features) into a 2D grid where similar data points cluster together.
This makes SOMs especially useful for:

Customer segmentation

Pattern recognition

Dimensionality reduction

Exploratory data analysis

