# Cryptocurrencies

## Resources
  Software: Python 3
  Libraries: Pandas, scikit-learn, hvplot
  
## Project Overview
  Using a dataset on Cryptocurrencies look for trends via unsupervised learning. The goals for this project are to:
  * Prepare the data for dimension reduction with PCA and clustering using K-Means.
  * Reduce data dimensions using PCA algorithsm from sklearn.
  * Predict clusters using cryptocurrencies data using the K-means algorithm from sklearn.
  * Create plots and data tables to present the results.
  
  The data is loaded into a pandas data frame where the data cleaning starts. Only current, actively traded, non-null cryptocurrencies are included in our target dataset. String columns **Algorithm** and **ProofType** are mapped into integers corresponding to their string values since unsupervised learning works with numerical data only. Once our target dataset is fully numeric the *StandardScaler()* function is applied which scales each column to have the same mean (at 0) and then scaling to unit variance.
   
   Once the data is scaled dimensionality can be reduced using Principal Component Analysis (PCA) with 3 components. This allows the dataset to be taken from 4 dimensions into 3 components occupying the same span. With 3 components established K-Means can be interably applied to obtain the **Elbow Curve** showing the sum of squared error (SSE) of different K-Means. 5-Mean clustering was chosen based off of the Elbow Curve. 
   
   With 5-Means clustering applied we're able to visualize the results of our clustering, and class labels for the 533 different types of cryptocurrencies that are being actively traded. We can also display the data in an hvplot table, as well as perform a scatter plot showing Total Coins Mined, and Total Coins Supply.
