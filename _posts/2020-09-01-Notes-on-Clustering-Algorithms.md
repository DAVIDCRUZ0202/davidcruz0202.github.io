---
layout: post
title: Notes on DBSCAN, OPTICS, and clustering algorithms
subtitle: an how companies utilize these algorithms for research and growth
---

In the world of unsupervised learning, whenever we have some data points of a graph, we try to make clusters of those points. Clusters help to group the most similar points in a distribution, based on the values held within those points. Think of one data point as one observation in a data set. When you have clusters established, whenever a new data point comes, we can predict which cluster it will fall into. Clustering algorithms work to accurately define these clusters, and different algorithms have been created. 

[DBSCAN](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.DBSCAN.html)is one of the more popular data clustering algorithms available. In a broad sense, an algorithm is any logical list of steps , encoded for a machine to interpret and, based on those steps, return a desired result. Read the wikipedia on [Algorithms](https://en.wikipedia.org/wiki/Algorithm) for clarification and in depth understanding. So , what is DBSCAN? Why is it useful for classification problems? What are the pros and cons for both?

DBSCAN stands for Density-Based Spatial Clustering of Applications with Noise. Each part of the name actually helps in understanding how the algorithm works, so let's evaluate a little deeper.

* Density Based - The algorithm calculates clusters based on the density of the data points when graphed. If points are tightly plotted together, with not much space in between each point, it can be said that there is a group of densely plotted points. This resulting group will be identified as a cluster by the algorithm. The opposite is also true; if points are plotted with large amounts of distance between them , then they wouldn't be considered to be part of the same cluster. 
* Spatial - This refers to the algorithm's calculation method. It scans for clusters in a spatial plane in relation to the data being graphed.
* Clustering - Another word for categorization. Clustering is the grouping of data points based on the density of their plotted positions.
* Applications - This is a synonym for data
* with Noise - This is a very important concept. Since DBSCAN functions through the plotting of points, any points which are outliers to the data will not fall in any cluster , these points will be labeled as Noise. It's good to remember this when learning how DBSCAN differs from OPTICS.

So, DBSCAN is a clustering algorithm which groups data observations into clusters based off a spatial plotting of the points, followed by the calculated distances betweent those points establishing the limits or borders each cluster. How does it do this? To follow through on what the algorithm does, I've broken it down into steps in the form of a list.

DBSCAN does the following to perform it's calculation.

1. Label the first core point. DBSCAN will choose a random point in the data set, and test it to see if it can serve as a core point. There are two parameters necessary to be passed into the algorithm for this to work.
    * Epsilon - This is the radial distance which is used to draw a circle around the test point.
    * Minpts(minimum points) - Minimum points establishes the amount of points which need to fall in the circle of the test point in order for it to become a core point.
To make a test point considered a core point, meet these two conditions. Set the boundary to be equal to the epsilon, and at least Minpts amount of points must be within that boundary.

2. Label all border points for the core point identified. Border points are all of the points which fall inside of a core point's boundary, but they themselves do not meet the criteria of having the minimum number of points for them to be core points themselves.

3. Once all border points have been identified, scan for a next random point which has not been tested, and repeat steps one and two.

4. Once all points have been visited, the algorithm has been completed and clustered.

What about Noise?

For all points which don't fall into any of the core point's boundaries, it gets identified as Noise, and is not passed into any cluster.

When core points are identified, all of the points within that point's boundary are either boundary points or core points themselves. It's very important to remember that only **Core Points** can create clusters, and only by being within the boundaries of a core point can a new point be identified as a border point. Border points cannot identify new border points! 

DBSCAN has been widely used because of it's ability to identify multiple clusters. It works well with noisy data, but it does have drawbacks. Higher dimensionality introduces problems for our algorithm, since it's based off of spatial plotting of points, algorithms have a problem when trying to plot points in exceedingly high dimensions. DBSCAN also knows how to identify noise, but there is a chance of random noise still being included in the clustered sets. It's typically used to identify high density clusters and separate them from low density clusters. It struggles with data sets containing various densities of clusters.

If you're interested in learning about more algorithms, I suggest learning about [OPTICS](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.OPTICS.html) first. It's closely related to DBSCAN and can serve as a great stepping stone to other clustering techniques. 

Clustering algorithms have a wide variety of use cases and have been used by various businesses across several industries. They serve very well in searching for patterns in data, as well as some different use cases like image processing, and very commonly in data mining. I highly suggest all practitioners of data science and ML to learn about these types of algorithms, and I'm extremely confident that most will think of a use case.