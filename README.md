# IITISOC-22_final
PS4 – Animal Image Clustering:

Develop a robust clustering implementation to tell apart the images of a wide range of animals given their images.
Understanding the Problem Statement
The problem involves clustering, hence comes under the domain of unsupervised learning.
Classification Vs Clustering – Both processes are used for the categorization of objects into one or more classes based on their features. However, minute their basic difference, it was crucial to comprehend the difference between the two to fully understand the problem statement.
In the case of classification, there are predefined labels assigned to each input instance according to their properties whereas in clustering those labels are missing. In essence, grouping the instances based on their similarity without any class labels is known as clustering.
The PS clearly mentions the use of clustering.
The Dataset
Specifications – Dataset includes 10 Types of Animals with 60 (colored) images of each.
Source: A subset of a Kaggle Dataset.
Approach-
Tools and Frameworks used – Tensorflow, Keras, SciKitLearn
Libraries used – Numpy, Panda, shutil, Matplotlib,kMeans, StandardScalar, PCA, silhouette_score.
Workflow:
1.  	Data Preprocessing
2.  	Feature Extraction – Using various pre-trained models for feature extraction and accepting the one with the highest accuracy.
·   	Instantiated a base model and loaded the pre-trained weights into it.
·   	Ran our dataset through it and recorded the output of the layer (excluding the top layer) to extract the features of each image.
3.  	Created a DataFrame of two columns with image names against image features.
4.  	Shuffled the data frame so that the model does not learn anything from the order of the images passed.
5.  	Applied PCA (Principal Component Analysis) to improvise the model
(Since it is necessary to normalize data before performing PCA, the StandardScaler function was used for normalization)
6.  	Implemented the kMeans Clustering Algorithm to cluster the images
7.  	Further, to test the model, we used the following evaluation method:
Silhouette score:
Metric: Euclidean distance
A negative silhouette score indicates wrong clustering.
While a positive silhouette score indicates correct clustering
For our model, we received the score of 0.0929
Since, this is an unsupervised learning algorithm, evaluation metrics are solely dependent on the density and distances between clusters. However, to check the accuracy of the model, we further decided to quantitatively analyze our results to calculate the same.
8.  	The number of images correctly grouped was counted for each cluster, to obtain the total number of correctly clustered images.
This gave us the accuracy: Total number of correctly clustered images/ Total number of images
Accuracy Chart:
The following is the accuracy chart for different models that we utilized:
Sr.no
   Model             Accuracy
1.InceptionResNetV3  0.8333
2.InceptionV3        0.7616
3.DenseNet169        0.6383

9. Storing clustered images in the Output directory:
Further, in the output directory, we created folders to store the clustered images.
Nine folders were created and the respective images were added to those folders.

Overall Experience:
This PS of IITISoC exposed us to the world of unsupervised learning and how it can be implemented and evaluated. Since none of us had worked on it before, we learned much about the concepts behind clustering and its evaluation.


 
 
 
 

 
 
 
 
 
