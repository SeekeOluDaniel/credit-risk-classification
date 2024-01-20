# credit-risk-classification

## Week 20 Challenge Report

### Overview of the Analysis

The purpose of this analysis is to train and evaluate a classification model of over 77,000 borrowers based on their loan risk. The objective was to use the provided dataset containing historical lending data from a lending services company to build a model that can identify the creditworthiness of its borrowing customers by classifying them into two classes: 0 (healthy loan) and 1 (high-risk loan).

Historically, from the full original dataset, 75036 of the 77536 loans are identified as healthy loans vs 2500 identified as high-risk. As part of this analysis, I took the following steps:
1. Separated the data into labels (loan status) and features (independent variables).
2. Split the data for the purpose of training and testing.
3. Created a logistic regression model, fitted the model using the original training data, and saved the predictions on the testing data labels.
4. Created a second logistic regression model using the resampled training data (with the random oversampler module), to fit the model and make predictions.


### Results

#### Model 1
Accuracy: The overall accuracy of the model is 0.99 (99%) while the balanced accuracy score is 0.9442 (94.4%).

Precision: The precision of a class is the ratio of correctly predicted instances of that class to the total instances predicted as that class. For class 0, the precision is 1.00 (100%), and for class 1, it is 0.87 (87%). High precision indicates a low rate of false positives.

Recall: Recall is the ratio of correctly predicted instances of a class to the total actual instances of that class. For class 0, the recall is 1.00 (100%), and for class 1, it is 0.89 (89%). High recall indicates a low rate of false negatives.

F1-score: The F1-score is the harmonic mean of precision and recall. It provides a balance between precision and recall. For class 0, the F1-score is 1.00, and for class 1, it is 0.88.

Support: The support is the number of actual occurrences of each class in the specified dataset. For class 0, there are 18,759 instances, and for class 1, there are 625 instances.



#### Model 2
Accuracy: Overall accuracy is 1.00 (100%), indicating that the model is making correct predictions for all instances in the dataset, while the balanced accuracy score is 0.9959 (99.6%).

Precision: Precision is the ratio of true positive predictions to the total positive predictions made by the model. For class 0, precision is perfect at 1.00, indicating that all instances predicted as class 0 were indeed class 0. For class 1, precision is 0.87, indicating that 87% of instances predicted as class 1 were truly class 1.

Recall: Recall is the ratio of true positive predictions to the total actual positives in the dataset. For both class 0 and class 1, recall is 1.00, indicating that the model is capturing all instances of both classes.

F1-score: F1-score is the harmonic mean of precision and recall. For class 0, the F1-score is 1.00, and for class 1, it is 0.93. F1-score provides a balance between precision and recall.


### Summary

Both models have a high precision of predicting both classes, with a higher ratio of correctly predicted "0"(healthy loans) vs "1"(high risk loans). Both models also have a similar precision rate of predicting high-risk loans (class 1), but model 2 has a higher balanced accuracy score and perfect recall for both classes.
Based on the foregoing, I would recommend the model with a higher balanced accuracy score, and perfect recall for both classes, which is Model 2 which also has an overall accuracy score of over 100%, and performs slightly better than Model 1.