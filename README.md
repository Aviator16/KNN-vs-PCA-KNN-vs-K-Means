# KNN-vs-PCA-KNN-vs-K-Means
A comparative study between the algorithms

The dataset used for this study is [Mushroom CLassification (Kaggle Dataset)](https://www.kaggle.com/uciml/mushroom-classification).

First I had to introduce dummy variables as  all the features were categorical variables of type char. I used Label Encoder for the purpose. I divided the dataset into data and target.
Then I split the data for training and testing  to be used in KNN and PCA algorithms.

#### I used the KNN algorithm first with no. of neighbours=3 and timed the fitting process:
The results were as follows:
* Time taken to fit KNN model was 0.0297874269999987 seconds.
* Accuracy of KNN model was 0.9993846153846154.

#### Next I used PCA to reduce the number of dimensions of the dataset and then applied KNN.
The results were as follows:
* After applying PCA the dimesnions of the dataset reduced from 22 to 14 and captured 99% if the variation.
* Time taken to fit KNN model after the PCA transformation was 0.010050101999997452 seconds.
* Accuracy of the model was 0.9987692307692307.

#### Lastly I used K-Means algorithm and set the number of clusters as 2 as I knew the classes beforehand. It is to be noted that K-Means is not a classification algorithm but a clustering algorithm hence it gives no imporatnce to the target variable.
The results were as follows:
* Time taken to fit K_Means clustering to data dataset is 0.3875107129999975 seconds.
* Accuracy of our K-Means model is 0.7090103397341211.

# Conclusion
* It can be clearly seen as expected KNN gives the highest accuracy among the 3 methods.
* The shortest time was taken by PCA+KNN method as we had reduced the number pf features in our dataset.
* K-Means is a clustering algorithm, an unsupervised form of learning and hence high accuracy was not expected but still gave a fairly good result.
