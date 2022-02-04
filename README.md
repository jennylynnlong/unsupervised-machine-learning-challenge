# Unsupervised Machine Learning Challenge: Cryptocurrency Clusters

## Details About the Challenge
This assignment was designed to challenge me to create a report that includes what cryptocurrencies are on the trading market and determine if they can be grouped to create a classification system by using several clustering algorithms and data visualization.

## Data Preparation
1. Read the [Crypto Dataset](/crypto_data.csv) from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist) into Pandas.
   - ![image](https://user-images.githubusercontent.com/88349512/152586773-1866107a-6bf1-4b4f-ac71-a7b29a959706.png)

2. Discard all cryptocurrencies that are not being traded and drop the IsTrading column from the dataframe.
   - ![image](https://user-images.githubusercontent.com/88349512/152586840-2489f034-2b4d-481d-a18f-23dc3e16e588.png)

3. Remove all rows with a null value.
   - ![image](https://user-images.githubusercontent.com/88349512/152586873-84e09ec3-375d-4da3-a949-2c87f71645e9.png)

4. Filter for cryptocurrencies that have been mined.
   - ![image](https://user-images.githubusercontent.com/88349512/152586929-af8446b8-73c7-4490-8147-8ea357422e68.png)

5. Convert data into numeric data and delete CoinName column.
   - ![image](https://user-images.githubusercontent.com/88349512/152587066-2af3814b-ac68-49b5-9feb-f4f5e77fc9a3.png)

6. Convert remaining features with text values into numerical data.
   - ![image](https://user-images.githubusercontent.com/88349512/152587118-cc584d32-53ff-4c43-bb15-8e3785a1541a.png)
   - It should be noted that the number of rows and columns in the dataset changed from 532 rows and 4 columns to 532 rows and 98 columns.

7. Standardize the dataset.
   - ![image](https://user-images.githubusercontent.com/88349512/152587245-d042d30d-12de-4008-889d-d66eea96dbdf.png)

## Dimensionality Reduction: PCA and t-SNE
1. Perform dimensionality reduction with PCA preserving 90% of the explained variance.
   - ![image](https://user-images.githubusercontent.com/88349512/152587347-e335a24b-2cb6-436e-8d80-f2496291ea08.png)
   - It should be noted that the number of features changed from 98 to 74.

2. Perform dimensionality reduction with t-SNE and create a scatter plot of the output.
   - ![image](https://user-images.githubusercontent.com/88349512/152587395-e8087bfc-edbb-4329-8214-efe7a37cd9d2.png)
   - ![image](https://user-images.githubusercontent.com/88349512/152587423-3b309eba-cab1-4868-be9e-8b9d51ce75b9.png)
     - There are not any distinct clusters in the t-SNE scatter plot.

## Cluster Analysis with k-Means
1. Use a for-loop to determine the inertia for each k between 1-10.
   - ![image](https://user-images.githubusercontent.com/88349512/152587586-e0e60a9d-6ce6-4197-af10-37f462752edb.png)

2. Create an elbow plot to identify the best number of clusters
   - ![image](https://user-images.githubusercontent.com/88349512/152587622-78c1748b-38dc-439b-b996-74c55496b2de.png)

3. Determine, if possible, where the elbow of the plot is and at which value of k it appears.
   - There is no elbow in this plot, so there are no meaningful clusters in the k-Means plot.

## Recommendation
- These cryptocurrencies can not be clustered together meaningfully. My recommendation is to not create a new investment portfolio by clusters, but rather diversify by randomly choosing cryptocurrencies or let your customers choose which cryptocurrency they'd like to invest in.

### Run the Code
1. Open and run the [Crypto Starter Jupyter Notebook](/crypto-Starter.ipynb) to see the above.
