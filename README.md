# DATA-VISUALIZATION

Dataset: MNIST dataset(Dataset of hand written numbers)<br>
We are going to use 2 techniques for Data visualization
* PCA
* TSNE
<br><br>manually 
**PCA**<br>
In PCA we are going to implement both manually and using sklearn library. While using the sklearn library we simply get the coordinates of the points on PC1 and PC2 and we simply plot them by making hue='labels'.<br>While manually implementing PCA we are going to find the covariance matrix of the dataset and then do eigen-decomposition of that covariance matrix. Upon eigen-decomposition we get a set of eigen values and corresponding eigen vectors. The eigen vector corresponding to the maximum eigen value is my PC1(the axis in which the variance of the data is maximum OR the data is most widely spread), then the next highest gives me the PC2. Then we project our whole dataset over these two new axes and do a scatter plot of those projections. PCA is a very nice dimensionality reduction techniques but we must keep in mind that * PCA doesn't look at class labels during projection
* PCA maximizes the global variance and doesn't look at shape[not 'topology preserving']