# Credit_Risk_Analysis

# Overview

Credit risk is very tough to predict. In this project we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high risk status. One method that data scientists use for this type of issue is creating a model and then evaluate and train the models that they create. In this specific project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

# Results


Balanced Random Forest Classifier results: the accuracy score is 87.5% the precision is 99% and the recall is 88%

<img width="1342" alt="Screen Shot 2021-06-27 at 10 28 01 PM" src="https://user-images.githubusercontent.com/79673185/123571271-dd6eed00-d797-11eb-8faf-5426aca86dcd.png">



Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94%

<img width="1343" alt="Screen Shot 2021-06-27 at 10 28 27 PM" src="https://user-images.githubusercontent.com/79673185/123571284-e495fb00-d797-11eb-8eb8-9ce55538c767.png">


Naive Random Oversampling results: Our balanced accuracy test it 65%, the precision for the high_risk has a very low positivity at 1% and the recall is 72%

<img width="1322" alt="Screen Shot 2021-06-27 at 10 29 03 PM" src="https://user-images.githubusercontent.com/79673185/123571296-ec559f80-d797-11eb-8255-45d11bf497ca.png">


SMOTE oversampling results: the accuracy score is 66.2%, the precision for the high_risk loans has a low positvity again at 1% and recall is 63% overall

<img width="1383" alt="Screen Shot 2021-06-27 at 10 29 35 PM" src="https://user-images.githubusercontent.com/79673185/123571307-f24b8080-d797-11eb-880e-981bbe6b3dd7.png">


Undersampling results: balanced accuracy score is 54.4% overall, the precision is at 99% and the recall is 40%

<img width="1407" alt="Screen Shot 2021-06-27 at 10 29 54 PM" src="https://user-images.githubusercontent.com/79673185/123571320-f8d9f800-d797-11eb-89bc-d6a029d09441.png">


Combination(over and undersampling) results: balanced accuracy score is 64.1% the precision is 99% and the recall is 57% overall

<img width="1364" alt="Screen Shot 2021-06-27 at 10 30 10 PM" src="https://user-images.githubusercontent.com/79673185/123571333-fe374280-d797-11eb-926d-493347cd2953.png">



# Summary


 The first two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. In the next four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.

