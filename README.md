# CSE151A_DARWIN_Alzheimer's

__Link to Dataset:__
Link to DARWIN dataset: [here](https://archive.ics.uci.edu/dataset/732/darwin)

__Abstract:__
Early diagnosis of Alzheimer's disease remains the primary means to delay brain damage and improve the quality of life of people affected, therefore, predicting which early diagnosis methods are most effective is ideal. The DARWIN dataset (Diagnosis AlzheimeR WIth haNdwriting) contains handwriting data from people affected by Alzheimer's, as well as people without Alzheimer's, and is the largest publicly available in terms of participants and handwriting tasks. This data is labeled, requiring supervised learning. It has 174 observations/instances collected from 174 participants, and 451 features, that are divided into 25 tasks. Our goal for this project is to leverage the DARWIN dataset to develop classification models that will evaluate which tasks are more effective at indicating Alzheimer's Disease, as well as the effectiveness of the specific features of each task. We plan to utilize methods such as logistic regression, perceptron, K-Nearest Neighbors, and Naive Bayes to accomplish this task. 

__Preprocessing Data:__
To first clean up the data, we searched for any NaN/invalid or missing values, but found none and did not have to do any imputation to fill the missing values. We then encoded the 'class' feature--whether an instance of data belongs to an Alzheimer's patient (P) or a healthy tester (H)--into binary values, with 1 for patient and 0 for healthy. The class feature is our target feature which we want to predict. Afterwards we created a list of datasets, where each item focuses on the data collected from a single writing test; there are 25 different tests total, each one with the same 18 basic features. We then looked at a pairplot for the basic features corresponding to the first of these writing tests; as well as a pairplot that compiled all the data across all tests for each basic feature, while color-coding the data for each test. Finally, we examined a heatmap of the correlation coefficients for the features from the first writing test. Our data was balanced, there was a near 50/50 split between patients (1) and healthy testers (0). 


