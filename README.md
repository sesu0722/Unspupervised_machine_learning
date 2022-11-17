# Myopia Clusters

I apply what I learned about unsupervised learning by fitting data to a model and using clustering algorithms to place data into groups. Then, create a visualization that shares my findings. 


This activity is broken down into four parts: 

* Part 1: Prepare the Data

* Part 2: Apply Dimensionality Reduction 

* Part 3: Perform a Cluster Analysis with K-means

* Part 4: Make a Recommendation 

### Part 1: Prepare the Data

1. Read `myopia.csv` into a Pandas DataFrame.

2. Remove the "MYOPIC" column from the dataset.

    * **Note:** The target column is needed for supervised machine learning, but it will make an unsupervised model biased. After all, the target column is effectively providing clusters already! 

3. Standardize the dataset so that columns that contain larger values do not influence the outcome more than columns with smaller values.

### Part 2: Apply Dimensionality Reduction

1. Perform dimensionality reduction with PCA.

2. Further reduce the dataset dimensions with t-SNE and visually inspect the results by runing t-SNE on the principal components, which is the output of the PCA transformation. 

3. Create a scatter plot of the t-SNE output.

![Screen Shot 2022-11-02 at 10 30 35 PM](https://user-images.githubusercontent.com/105521221/199637215-8a1562cc-a7bf-4ca2-8650-858906729d7f.png)

### Part 3: Perform a Cluster Analysis with K-means

Create an elbow plot to identify the best number of clusters. Make sure to do the following:

* Use a `for` loop to determine the inertia for each `k` between 1 through 10. 

* Determine where the elbow of the plot is, and at which value of `k` it appears.

![Screen Shot 2022-11-02 at 10 37 17 PM](https://user-images.githubusercontent.com/105521221/199637757-03434e45-eb75-4fe4-a587-e4ead4e40b7a.png)


### Part 4: Make a Recommendation

Can the patients be clustered?

* From the TSNE plot, the two clusters are positioned overlaping together and inconclusive to determine if the patients can be clustered into whether the kids have or does not have myopic. 

* From the elbow polt, the best number of clusters is 3. However, the inertia is still high at this point and slowly decrease after.

