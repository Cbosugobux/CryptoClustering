Module 19, Crypto Clustering

In this exercise, students were asked to create visualizations using the Unsupervised module "KMeans."

The first step was to import the "crypto_market_data" CSV and then using StandardScaler, normalize the data.  After, students created a dataframe with the scaled
data and set the index to the "coin_id". To confirm this happened correctly, we used the .head() property from Pandas to view the first five rows.

Following this, to help set up our KMeans model, we created a list where k values were established between 1 and 11.  Then we stored the inertia values in another list.  Looping through the data, we computed the interia with each possible value of k.  After finding these values, we created a dictionary in or to plot the data to an elbow curve.  Plotting a line chart "elbow curve" and seeing where the most extreme elbow occured, we were able to determine the best value of k = 4.

Knowing this, we created a K-means model using the scaled dataframe.  We initialized the model with the k=4 value and then fitted it to our scaled dataframe.

After doing this we were able to predict clusters to group the crypto currencies. To add these values to the dataframe, we created a copy of the scaled data and added the column "CryptoClusters" to the df.

We then created a scatterplot setting the x-axis to price_change_percentage_24h and the y-axis to price_change_percentage_7d

Following this, we used Principal Component Analysis to optimize our clusters.  Reducing the scaled dataframe to three principal components, we collowed the same steps outlined above.  The explained variance by the PCA was around 90%.

After finding the best value of k to be '4' again, we created a K-Means model, fit, predicted and plotted the clusters.

We combined the Elbow Plots and the Cluster Plots from both analyses.  



