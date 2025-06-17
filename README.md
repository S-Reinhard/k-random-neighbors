# k-random-neighbors
A Monto-Carlo Approach to classififation by using scattered data points

**To run the code on your machine follow the guide in [setup.md](setup.md)**

This notebook introduces a randomized classification method for data points based on attribute guessing. The approach works as follows:

The training data is already classified and is considered as a point cloud in a coordinate system. The features serve as the axes of this coordinate system. The classes of the data points are placed at specific positions within the coordinate system. The exact position of a class is determined by the feature values of the data point.

To determine the class of a data point that has not yet been classified, the algorithm searches for classes at random positions that are normally distributed around point X within the coordinate system. It continues searching until it has found at least k classes. To assign a unique class to X, the mode of the found classes is used.

The idea behind this is similar to k-nearest neighbors (k-NN), where the similarity of data points is determined by their distance from one another. However, traditional algorithms like k-NN must compute the distance between all points, which does not scale well with a large number of data points. This approach to class selection is intended to overcome this scalability issue.
