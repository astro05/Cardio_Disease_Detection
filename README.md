Heart Disease Prediction using Machine Learning & Deep Neural Network Models

1. Introduction

Cardiac disorders also known narrowly as “heart diseases” are the cause of most deaths worldwide. Heart disease has become a cause of increasing concern for this country with patients enduring several sorts of related illnesses. Death is inevitable if some of the related diseases are diagnosed too late.

In our project, we will try to generate a predictive model of heart diseases which will be used for early detections. Our focus is to find the pre-processing techniques best for specific models, improving the existing models, creating combined predictions from two or more datasets.Our Focus is to implement the model and increase the  accuracy of the model done previously.



1. Methodology

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.001.png)

`           `Fig: Proposed Methodology for this work


1. *Model Selection*

We have selected Artificial Neural Network(ANN), Convolutional Neural Network(CNN) and Long Short Term Memory (LSTM) for training our data based on  paper study. Our Focus is to implement the model and increase the  accuracy of the model done previously.





Model 4 (ANN)

Input Data Shape : 13. Input Data is scaled.  No. hidden layer : 1. Neurons: 300

Activation: 

Hidden Layer: Relu Output Layer: Sigmoid

` `Loss: Binary Cross Entropy with LogitLoss 


Model 5 (ANN)

Input Data Shape : 13. Input Data is scaled.  No. hidden layer : 1. Neurons: 300

Activation: 

Hidden Layer: Relu Output Layer: Sigmoid

` `Loss: Binary Cross Entropy with LogitLoss 

Output Shape: 1                  

















1. Experiments


This dataset was taken from the UCI machine learning repository. The heart disease dataset is made up of 75 raw features from which 13 features were published. These features are very vital in the diagnosis of heart diseases. The 13 features considered in this research work are stated

below :

1. *Dataset Collection*

***UCI Dataset:***


|**SI**|**Attributes**|**Description**|
| :-: | :-: | :-: |
|1.|Age|age in years|
|2.|Sex|1 = male; 0 = female|
|3.|cp|chest pain** type (4 values)|
|4.|trestbps|resting blood pressure (in mm Hg on admission to the hospital)|
|5.|chol|serum cholesterol in mg/dl|
|6.|fbs|(fasting blood sugar &gt; 120 mg/dl) (1 = true; 0 = false)|
|7.|restecg|resting electrocardiographic results|
|8.|Thalach|maximum heart rate achieved|
|9.|Exang|exercise induced angina (1 = yes; 0 = no)|
|10.|Oldpeak|ST depression induced by exercise relative to rest|
|11.|Slope|Heart rate slope|
|12.|Ca|Count of major vessels (value 0-3) coloured by fluoroscopy.|
|13.|Thal|<p>Thal: 3= normal; 6 = fixed defect; 7 = reversible defect.</p><p></p>|


The data set had 13 features and 303 rows. No NULL values or duplicate values found in the dataset. Dataset contains 164 (54.3%) heart disease (target = 1) patients and 138 (45.7%) non heart disease (target = 0) patients. Fig.1 represents a balanced dataset. Among these 31.79 % are Female Patients and 68.21 % are Male Patients. The average age of patients is 53. Fig.2 shows the patients affected in cardiac disease at different ranges of age. From Fig.3 visualized that the affected rate of male patients is higher than the rate of female patients.

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.002.png) 

`   `Fig.1: Heart disease(1) and Non heart disease(0)

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.003.png)

`   `Fig.2: Age vs Cardio Disease.


![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.004.png)

Fig.3: Affected patient based on sex.


***Cardiovascular\_Dataset:***
\***


|**SI**|**Attributes**|**Description**|
| :- | :- | :- |
|1.|age|Objective Feature. int (days)|
|2.|height|Objective Feature. int (cm) |
|3.|weight|Objective Feature. float (kg) |
|4.|Gender|Objective Feature. Categorical code(1 - women, 2 - men)|
|5.|ap\_hi|Systolic blood pressure. Examination Feature.  int |
|6.|ap\_lo|Diastolic blood pressure. Examination Feature.  int |
|7.|cholesterol|Cholesterol. Examination Feature(1: normal, 2: above normal, 3: well above normal) |
|8.|gluc|Glucose. Examination Feature ( 1: normal, 2: above normal, 3: well above normal)|
|9.|smoke|Smoking. Subjective Feature. binary|
|10.|alco |Alcohol intake. Subjective Feature.  binary|
|11.|active|Physical activity. Subjective Feature.  binary |

The data set had 11 features and 70000 rows. There are 3 types of input features:

Objective: factual information.

Examination: results of medical examination.

Subjective: information given by the patient.

No NULL values or duplicate values found in the dataset. Dataset contains 34979 (49.97%) heart disease (cardio = 1) patients and 35021(50.03 %) non heart disease (cardio = 0) patients. Fig.5 represents a balanced dataset. Among these 34.96% are Female Patients and 65.04% are Male Patients. The average age of patients is 55. Fig.6 shows the patients affected in cardiac disease at different ranges of age. Fig.7 visualized that the affected rate of male patients is higher than the rate of female patients.


![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.005.png) 

`   `Fig.5: Heart disease(1) and Non heart disease(0)

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.006.png)

`   `Fig.6: Age vs Cardio Disease.


![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.007.png)

Fig.7: Affected patient based on sex.




1. *Data Pre-Processing*

To increase the performance and stability need to pre processing the data. The SelectKBest method selects the features according to the k highest score. Applying fclassif  chol (2.002%),fbs (0.2160%), trestbps (6.55%) have low scores and drop these features. Now it has 10 features and 210 rows. KNN

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.008.png)

Fig.4: Feature Score (Least Important Selected)



1. *Performance Metrics*

   For *Performance Metrics we have taken Accuracy , Precision , Recall, F1  Score for evaluation of models.*

   The paper we have chosen to improve firstly was Neural network diagnosis of heart disease (2015). Our expected result is 85% accuracy after implementing the mentioned structure.
   As we successfully improved the model given and increased the accuracy of the selected paper we tried to select two more papers with better performance metrics. As we know, only accuracy can not be a good performance metric for heart disease prediction.

Our Result:

Logistic Regression(Best Result): Accuracy 91.20%

Decision Tree : Accuracy 84.62%

KNN : Accuracy 79.00%

SVM: Accuracy 86.81%

Random Forest: Accuracy 86.81%

Perceptron : Accuracy 83.54%

Gradient Boosting: Accuracy 86.81%

*Confusion Matrix*
\*

\*


||*Predicted Positive*|*Predicted Negative*|
| :- | :- | :- |
|*Actual Positive*|*35*|*0*|
|*Actual Negative*|*3*|*23*|






*Result Comparison from Previous Studies*


|Paper|Model|Accuracy|Precision |Recall|F1-Score|
| :- | :- | :- | :- | :- | :- |
|*Olaniyi, E. O., Oyedotun, O. K., Helwan, A., & Adnan, K. (2015). Neural network diagnosis of heart disease.*|<p></p><p></p><p>Decision Tree</p><p></p><p>Naive Bayes</p>|<p>45.67%</p><p></p><p>84.35%</p><p></p><p>82.31%</p>||||
|*Tasnim, F., & Habiba, S. U. (2021). A Comparative Study on Heart Disease Prediction Using Data Mining Techniques and Feature Selection. 2021 2nd International Conference on Robotics, Electrical and Signal Processing Techniques* |<p>KNN</p><p>SVM</p><p></p><p>Logistic Regression</p><p></p><p>Gradient Boosting</p><p></p><p>Random Forest</p>|<p>88%</p><p>82%</p><p></p><p>80%</p><p></p><p>83%</p><p></p><p></p><p>91.17%</p>|<p>87%</p><p>83%</p><p></p><p>82%</p><p></p><p>82%</p><p></p><p></p><p>91%</p>|<p>86%</p><p>81%</p><p></p><p>81%</p><p></p><p>80%</p><p></p><p></p><p>90%</p>||
|||||||
|*Terrada, O., Cherradi, B., Hamida, S., Raihani, A., Moujahid, H., & Bouattane, O. (2020). Prediction of Patients with Heart Disease using Artificial Neural Network and Adaptive Boosting techniques. 2020*|<p>AdaBoost</p><p></p><p></p>|72.22%|69.57% |66.67%|68.09%|

`                                   		  	`Table: *Previous Result*














***UCI Data Set Result***



|<p></p><p>Model Name</p>|<p></p><p>Preprocessing</p>|`                                              `Result|
| :- | :- | :- |
|||Accuracy |Precision|Recall|F1 Score|
|Logistic Regression|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>Chi-square</p><p></p><p>One Hot Encoding</p>|<p>87.91%</p><p></p><p></p><p>87.91%</p><p></p><p></p><p>90.11%</p><p></p><p></p><p>85.71%</p><p></p><p>90.11%</p>|<p>88.23%</p><p></p><p></p><p>88.23%</p><p></p><p></p><p>90.48%</p><p></p><p>85.69%</p><p></p><p></p><p>90.10%</p>|<p>87.91%</p><p></p><p></p><p>87.91%</p><p></p><p></p><p>90.11%</p><p></p><p>85.71%</p><p></p><p></p><p>90.11%</p>|<p>87.79%</p><p></p><p></p><p>87.79%</p><p></p><p></p><p>90.01%</p><p></p><p>85.69%</p><p></p><p></p><p>90.10%</p>|
|Decision Tree|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>Chi-square</p><p></p><p>One Hot Encoding</p>|<p>71.43%</p><p></p><p></p><p>75.82%</p><p></p><p></p><p>79.12%</p><p></p><p>80.22%</p><p></p><p></p><p>70.33%</p>|<p>71.32%</p><p></p><p></p><p>76.28%</p><p></p><p></p><p>79.41%</p><p></p><p>80.22%</p><p></p><p></p><p>70.66%</p>|<p>71.43%</p><p></p><p></p><p>75.82%</p><p></p><p></p><p>79.12%</p><p></p><p>80.22%</p><p></p><p></p><p>70.33%</p>|<p>71.34%</p><p></p><p></p><p>75.91%</p><p></p><p></p><p>79.18%</p><p></p><p>80.22%</p><p></p><p></p><p>70.42%</p>|
|KNN|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>Chi-square</p><p></p><p>One Hot Encoding</p>|<p>68.13%</p><p></p><p></p><p>84.62%</p><p></p><p></p><p>68.13%</p><p></p><p>68.13%</p><p></p><p></p><p>84.62%</p>|<p>68.05%</p><p></p><p></p><p>84.60%</p><p></p><p></p><p>68.05%</p><p></p><p>68.05%</p><p></p><p></p><p>84.62%</p>|<p>68.13%</p><p></p><p></p><p>84.62%</p><p></p><p></p><p>68.13%</p><p></p><p>68.13%</p><p></p><p></p><p>84.62%</p>|<p>68.08%</p><p></p><p></p><p>84.57%</p><p></p><p></p><p>68.08%</p><p></p><p>68.08%</p><p></p><p></p><p>84.62%</p>|
|SVM|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>Chi-square</p><p></p><p>One Hot Encoding</p>|<p>86.81%</p><p></p><p></p><p>87.91%</p><p></p><p></p><p>87.91%</p><p></p><p></p><p>86.81%</p><p></p><p>86.81%</p>|<p>86.96%</p><p></p><p></p><p>87.98%</p><p></p><p></p><p>88.23%</p><p></p><p></p><p>86.96%</p><p></p><p>86.96%</p>|<p>86.81%</p><p></p><p></p><p>87.91%</p><p></p><p></p><p>87.91%</p><p></p><p></p><p>86.81%</p><p></p><p>86.81%</p>|<p>86.71%</p><p></p><p></p><p>87.85%</p><p></p><p></p><p>87.79%</p><p></p><p></p><p>86.71%</p><p></p><p>86.71%</p>|
|Random Forest|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>Chi-square</p><p></p><p>One Hot Encoding</p>|<p>86.81%</p><p></p><p></p><p>83.52%</p><p></p><p>84.62%</p><p></p><p></p><p>83.52%</p><p></p><p></p><p>87.91%</p>|<p>86.81%</p><p></p><p></p><p>83.49%</p><p></p><p>84.60%</p><p></p><p></p><p>83.49%</p><p></p><p></p><p>87.96%</p>|<p>86.81%</p><p></p><p></p><p>83.52%</p><p></p><p>84.62%</p><p></p><p></p><p>83.52%</p><p></p><p></p><p>87.91%</p>|<p>86.81%</p><p></p><p></p><p>83.49%</p><p></p><p>84.57%</p><p></p><p></p><p>83.49%</p><p></p><p></p><p>87.93%</p>|
|Perceptron|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>Chi-square</p><p></p><p>One Hot Encoding</p>|<p>67.03%</p><p></p><p></p><p>76.92%</p><p></p><p></p><p>57.14%</p><p></p><p>68.13%</p><p></p><p></p><p>83.52%</p>|<p>69.97%</p><p></p><p></p><p>82.05%</p><p></p><p></p><p>75.71%</p><p></p><p>67.95%</p><p></p><p></p><p>83.58%</p>|<p>67.03%</p><p></p><p></p><p>76.92%</p><p></p><p></p><p>57.14%</p><p></p><p>68.13%</p><p></p><p></p><p>83.52%</p>|<p>66.87%</p><p></p><p></p><p>76.64%</p><p></p><p></p><p>42.69%</p><p></p><p>67.97%</p><p></p><p></p><p>83.54%</p>|
|Gradient Boosting|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>Chi-square</p><p></p><p>One Hot Encoding</p>|<p>86.81%</p><p></p><p></p><p>86.81%</p><p></p><p></p><p>85.71%</p><p></p><p></p><p>82.42%</p><p></p><p>84.62%</p>|<p>86.81%</p><p></p><p></p><p>86.81%</p><p></p><p></p><p>85.69%</p><p></p><p></p><p>82.57%</p><p></p><p>85.0%</p>|<p>86.81%</p><p></p><p></p><p>86.81%</p><p></p><p></p><p>85.71%</p><p></p><p></p><p>82.42%</p><p></p><p>84.62%</p>|<p>86.81%</p><p></p><p></p><p>86.77%</p><p></p><p></p><p>85.69%</p><p></p><p></p><p>82.46%</p><p></p><p>84.42%</p>|

















***Cardiovascular Data Set Result***


|<p></p><p>Model Name</p>|<p></p><p>Preprocessing</p>|`                                              `Result|
| :- | :- | :- |
|||Accuracy |Precision|Recall|F1 Score|
|Logistic Regression|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>One Hot Encoding</p>|<p>69.42%</p><p></p><p></p><p>49.89%</p><p></p><p></p><p>71.86%</p><p></p><p></p><p>49.89%</p>|<p>69.48%</p><p></p><p></p><p>24.89%</p><p></p><p></p><p>71.97%</p><p></p><p></p><p>24.89%</p>|<p>69.42%</p><p></p><p></p><p>49.89%</p><p></p><p></p><p>71.86%</p><p></p><p></p><p>49.89%</p>|<p>69.40%</p><p></p><p></p><p>33.21%</p><p></p><p></p><p>71.82%</p><p></p><p></p><p>33.21%</p>|
|Decision Tree|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>One Hot Encoding</p>|<p>63.31%</p><p></p><p></p><p>63.19%</p><p></p><p></p><p>63.50%</p><p></p><p></p><p>63.22%</p>|<p>61.72%</p><p></p><p></p><p>56.82%</p><p></p><p></p><p>63.81%</p><p></p><p></p><p>63.66%</p>|<p>63.43%</p><p></p><p></p><p>63.82%</p><p></p><p></p><p>63.12%</p><p></p><p></p><p>61.33%</p>|<p>61.34%</p><p></p><p></p><p>55.91%</p><p></p><p></p><p>61.18%</p><p></p><p></p><p>62.42%</p>|
|KNN|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>One Hot Encoding</p>|<p>63.79%</p><p></p><p></p><p>50.51%</p><p></p><p></p><p>68.93%</p><p></p><p></p><p>50.38%</p>|<p>63.93%</p><p></p><p></p><p>50.51%</p><p></p><p></p><p>68.95%</p><p></p><p></p><p>50.37%</p>|<p>63.79%</p><p></p><p></p><p>50.51%</p><p></p><p></p><p>68.93%</p><p></p><p></p><p>50.38%</p>|<p>63.69%</p><p></p><p></p><p>50.51%</p><p></p><p></p><p>68.92%</p><p></p><p></p><p>50.37%</p>|
|SVM|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>One Hot Encoding</p>|<p>71.66%</p><p></p><p></p><p>64.40%</p><p></p><p></p><p>72.30%</p><p></p><p></p><p>63.70%</p>|<p>71.77%</p><p></p><p></p><p>64.50%</p><p></p><p></p><p>72.94%</p><p></p><p></p><p>64.25%</p>|<p>71.66%</p><p></p><p></p><p>64.40%</p><p></p><p></p><p>72.30%</p><p></p><p></p><p>63.70%</p>|<p>71.62%</p><p></p><p></p><p>64.34%</p><p></p><p></p><p>72.09%</p><p></p><p></p><p>63.32%</p>|
|Random Forest|<p>All Feature</p><p></p><p>Scaling</p><p></p><p>FClassif</p><p></p><p>One Hot Encoding</p>|<p>71.96%</p><p></p><p></p><p>71.98%</p><p></p><p></p><p>70.48%</p><p></p><p></p><p>71.74%</p>|<p>71.99%</p><p></p><p></p><p>72.01%</p><p></p><p></p><p>70.48%</p><p></p><p></p><p>71.76%</p>|<p>71.96%</p><p></p><p></p><p>71.98%</p><p></p><p></p><p>70.48%</p><p></p><p></p><p>71.74%</p>|<p>71.95%</p><p></p><p></p><p>71.97%</p><p></p><p></p><p>70.48%</p><p></p><p></p><p>71.73%</p>|

`                                               		     `Table: *Our Result*






![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.009.png)

`                                                            `Fig. UCI Dataset Result Comparison

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.010.png)

`                                         `Fig. Cardio\_vascular Dataset Result Comparison

1. *Performance Metrics*

   For *Performance Metrics we have taken Accuracy , Precision , Recall, F1  Score for evaluation of models.*

   The paper we have chosen to improve firstly was Neural network diagnosis of heart disease (2015). Our expected result is 85% accuracy after implementing the mentioned structure.
   As we successfully improved the model given and increased the accuracy of the selected paper we tried to select two more papers with better performance metrics. As we know, only accuracy can not be a good performance metric for heart disease prediction.

Our Result:

ANN(Paper Structure) : Accuracy 85.71%

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.011.png)![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.012.png)

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.013.png)



ANN(Model 4) : Accuracy 91.08%

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.014.png)![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.015.png)

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.016.png)


ANN(Best Result) : Accuracy 95.08%

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.017.png)![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.018.png)

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.019.png)

*Confusion Matrix*
\*

\*


||*Predicted Positive*|*Predicted Negative*|
| :- | :- | :- |
|*Actual Positive*|*35*|*0*|
|*Actual Negative*|*3*|*23*|













*Result Comparison*


|Paper|Model|Accuracy|Precision |Recall|F1-Score|No Of Hidden Lair|
| :- | :- | :- | :- | :- | :- | :- |
|*Olaniyi, E. O., Oyedotun, O. K., Helwan, A., & Adnan, K. (2015). Neural network diagnosis of heart disease.*|ANN|85%||||6|
|*Lin, C.-H., Yang, P.-K., Lin, Y.-C., & Fu, P.-K. (2020). On Machine Learning Models for Heart Disease Diagnosis. 2020 IEEE 2nd Eurasia* |ANN|91.26%||||1|
||<p>CNN</p><p></p><p></p><p></p><p></p><p></p>|83.50%||||3|
|*Terrada, O., Cherradi, B., Hamida, S., Raihani, A., Moujahid, H., & Bouattane, O. (2020). Prediction of Patients with Heart Disease using Artificial Neural Network and Adaptive Boosting techniques. 2020*|ANN|91.41%|79.67%|70.36%|75.98%|3|

`                                   		  	`Table: *Previous Result*















1. *Evaluation*


|<p></p><p>Model Name</p>|<p></p><p>Preprocessing</p>|<p></p><p>No of Input Layer</p>|<p></p><p>No of Hidden Layer</p>|<p></p><p>Neurons/Filters</p>|<p>Activation Function &</p><p>Loss Function </p>|<p>Optimizer</p><p>&</p><p>Learning Rate</p>|Epoch|Result|
| :- | :- | :- | :- | :- | :- | :- | :- | :-: |
|||||||||Accuracy |Precision|Recall|F1 Score|<p>AUC</p><p>Score</p>|
|ANN (Paper Selected)|Scaling|13|6|5|<p></p><p>*Sigmoid*</p><p></p><p>` `*MSE*</p>|<p>*Adam*</p><p></p><p>*0.0032*</p>|2000|85.71%|84.41%|85.71%|85.05%|86%|
|ANN (Proposed Model-1)|Scaling|13|3|12|<p>*Relu*</p><p></p><p>*BCE*</p>|<p>*Adam*</p><p></p><p>*0.01*</p>|200|87.91%|88.17%|87.91%|87.95%|93%|
|LSTM (Model-2)|Scaling|13|4|100|<p>*Relu*</p><p></p><p>*BCE*</p>|<p>*Adam*</p><p></p><p>*0.001*</p>|90|77.04%|83.33%|73.53%|78.12%|78%|
|1D CNN (Proposed Model-3)|Scaling|13|2|128|<p>*Relu*</p><p></p><p>*BCE*</p>|<p>*Adam*</p><p></p><p>*0.01*</p>|15|86.81%|86.81%|86.81%|86.77%|86%|
|ANN (Proposed Model-4)|Feature Selection with Scaling|10|3|100|<p>*Relu*</p><p></p><p>*BCE*</p>|<p>*Adam*</p><p></p><p>*0.01*</p>|125|91.21%|91.44%|91.21%|91.14%|91%|
|<p>ANN (Proposed Model-5)</p><p>Best Result</p>|Scaling|13|1|300|<p>*Relu*</p><p></p><p>*BCE with LogitLoss*</p>|<p>*SGD*</p><p></p><p></p><p>*0.01*</p>|80|96.72%|100%|92.31%|96%|96%|


`                                               		     `Table: *Our Result*

![](img/Aspose.Words.1d1e64d0-4fc5-4b76-81b6-44c4ea1230ce.020.png)





1. Discussion

Our Experiment yielded good results.We have successfully obtained better results than above mentioned papers.We have found that generally scaling and encoding performs well for KNN,Logistic Regression.  In future performing more hyperparameter tuning may increase our result. Other Boosting algorithms can be used to increase the accuracy of the models.



