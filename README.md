# KNN Classifier and Data Pre-processing
Small project to apply basic data exploring, pre-processing, and cleaning. Then build a KNN classification model and compare performance


## Specific Objectives:
- Load datasets and perform some exploratory plots.
- Study how to apply some of basic data cleaning and preprocessing techniques.
- Gain experience on the use of moments. 
- Build KNN classifier and explore performance evaluation and metrics.
 
 
## KNN Classifier
The k-nearest neighbors (KNN) algorithm is a simple, easy-to-implement supervised machine learning algorithm that can be used to solve both classification and regression problems, it is more widely used in classification problems in the industry. The KNN algorithm assumes that similar things exist in close proximity. it works on a principle assuming every data point falling in near to each other is falling in the same class. In other words, it classifies a new data point based on similarity.

KNN algorithms decide a number k which is the nearest Neighbor to that data point that is to be classified. If the value of k is 5 it will look for 5 nearest Neighbors to that data point.The simple version of the K-nearest neighbour classifier algorithms is to predict the target label by finding the nearest neighbour class. The closest class to the point which is to be classified is calculated using Euclidean distance. 
 
 
## Datasets:
**Iris Dataset:** This dataset is a classic and fairly simple benchmark for basic machine learning algorithms. It includes different features (attributes) of three Iris flower species (setosa, versicolor, virginica). The rows being the samples (50) and the columns being: Sepal Length, Sepal Width, Petal Length and Petal Width

**Heart Dataset:** The dataset contains 14 features (attributes) and 303 instances. The features are multivariate with types - categorical, numeric, ordinal, binary. The target is a binary variable indicating the presence and absence of heart disease using 1 and 0 respectively.
 
 
## Part 1: Data Exploration
- Generate a “pairs plot” (also called a scatter plot matrix) of the data. From the pair plot, identify the subplots corresponding to the pairs of features where correlation is seen.
- Calculate and report the correlation coefficient for the pair of features.
- Calculate the mean, variance, skew, kurtosis for the datasets and observe the nature of data and the relationships between the features of the dataset.
- Detect outliers
- Group the features by their variable types and plot a histogram of the features to determine the number of present and absent heart disease cases.
- Data Cleaning: deal with any missing values in the data and remove any noise from the data by applying smoothing on some features. 
 
 
## Part 2: KNN Implementation and Performance Evaluation
Classify the data using a KNN classifier. Tune the parameter of the KNN classifier using sklearn functions, plot the different validation accuracies
against the values of the parameter, select the best parameter to fit the model and Report the resulting accuracy. Carry out the following activities and reporting:
 
### (1) Basic model:
- Divide the data into train, validation, and test sets (60%, 20%, 20%), set the random seed for splitting, use random state=275.
- Train the model with the classifier’s default parameters. Use the train set and test the model on the test set. Store the accuracy of the model.
- Find the best parameters for the classifier, in this case,k for KNN. To find the best parameter:
    - Test the following values of k for validation k: {1, 5, 10, 15, 20, 25, 30, 35}.
    - Fit the model using the train set.
    - Test the model with the validation set. Store the accuracy.
    - Plot a figure that shows the validation relationship between the accuracy and the parameter.
    - Report the best k in terms of classification accuracy.
- Using the best found parameters, fit the model using the training set and predict the target on the test set.
- Report the accuracy, AUC, f-score of the kNN classifier.
 
### (2) Improved Model:
Try to improve the classification results using performance metrics by exploring different ways to improve using the validation set.
- **Normalization:** Normalize the data using Z-Score normalization and explore its effect on performance.
- **Weighted KNN:** The KNeighborsClassifier class has an option for weighted KNN where points that are nearby to the query point are more important for the classification than others. Use different weighting schemes (default, manhatten, eculidean) to see the effect.
- After making these improvements compute the new classification results on the test set and report the accuracy, AUC and f-score.
