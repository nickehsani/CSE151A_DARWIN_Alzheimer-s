# CSE151A_DARWIN_Alzheimer's

Link to Final Report: [here](https://github.com/nickehsani/CSE151A_DARWIN_Alzheimer-s/blob/main/Written_Report.ipynb)

__Introduction:__
Early diagnosis of Alzheimer's disease remains the primary means to delay brain damage and improve the quality of life of people affected, therefore, predicting which early diagnosis methods are most effective is ideal. The DARWIN dataset (Diagnosis AlzheimeR WIth haNdwriting) contains handwriting data from people affected by Alzheimer's, as well as people without Alzheimer's, and is the largest publicly available in terms of participants and handwriting tasks. Our goal for this project was to leverage the DARWIN dataset to develop classification models that will evaluate which tasks are more effective at indicating Alzheimer's Disease, as well as the effectiveness of the specific features of each task.

__Link to Dataset:__
Link to DARWIN dataset: [here](https://archive.ics.uci.edu/dataset/732/darwin)

__Abstract:__
Early diagnosis of Alzheimer's disease remains the primary means to delay brain damage and improve the quality of life of people affected, therefore, predicting which early diagnosis methods are most effective is ideal. The DARWIN dataset (Diagnosis AlzheimeR WIth haNdwriting) contains handwriting data from people affected by Alzheimer's, as well as people without Alzheimer's, and is the largest publicly available in terms of participants and handwriting tasks. This data is labeled, requiring supervised learning. It has 174 observations/instances collected from 174 participants, and 451 features, that are divided into 25 tasks. Our goal for this project is to leverage the DARWIN dataset to develop classification models that will evaluate which tasks are more effective at indicating Alzheimer's Disease, as well as the effectiveness of the specific features of each task. We plan to utilize methods such as logistic regression, perceptron, K-Nearest Neighbors, and Naive Bayes to accomplish this task. 

__Preprocessing Data:__
To first clean up the data, we searched for any NaN/invalid or missing values, but found none and did not have to do any imputation to fill the missing values. We then encoded the 'class' feature--whether an instance of data belongs to an Alzheimer's patient (P) or a healthy tester (H)--into binary values, with 1 for patient and 0 for healthy. The class feature is our target feature which we want to predict. Afterwards we created a list of datasets, where each item focuses on the data collected from a single writing test; there are 25 different tests total, each one with the same 18 basic features. We then looked at a pairplot for the basic features corresponding to the first of these writing tests; as well as a pairplot that compiled all the data across all tests for each basic feature, while color-coding the data for each test. Finally, we examined a heatmap of the correlation coefficients for the features from the first writing test. Our data was balanced, there was a near 50/50 split between patients (1) and healthy testers (0). 

To finish processing the data, we tested for normality using shapiro tests, and found that very few of the columns were normally distributed. Therefore, we decided to minmax normalize our data after splitting it into X and Y datasets. 

__Logistic Regression:__
We used logistic regression as our first model. We split the dataset into 80% training and 20% test and trained a logistic regression model with 1000 iterations. Running the model on our test data returned 86% accuracy. On our training dataset, it returned 100% accuracy. On a fitting graph for this dataset, the logistic regression would fall on the lower end of model complexity. However, because the accuracy of the training dataset is 100%, while the test accuracy is much lower, it appears that this model may be overfit to the data. It would be helpful to see how future models perform given this same data. The next models we plan to use are a perceptron, K-Nearest Neighbors, and Naive Bayes, because we are trying to perform a binary classification task, and we want to explore how more complex models perform.

__Perceptron:__ We used a Perceptron as our second model. We split the dataset 80-20 training and testing data, and then we trained the Perceptron model using 20 epochs. On the training dataset, the accuracy was 100%, and on the testing data, the final model accuracy was 89%. We used Hinge loss on this model because it helps maximize margins between the two output classes. The Hinge loss of this model was 0.51. The top 5 largest absolute value weights corresponded to the features pressure_var19, mean_jerk_on_paper9, air_time13, mean_jerk_on_paper8, and gmrt_on_paper2. 


