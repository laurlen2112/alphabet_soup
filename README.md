# Neural Network Charity Analysis

## Overview:
The purpose of this is analysis is to use a neural network to predict the success of applicants should they be funded by Alphabet Soup.  The data file is a CSV containing information on over 34,000 organizations.  This analysis is comprised of two broad steps.  The first step pre-processes the code and runs it through a neural network.  The second step attempts various methods to optimize the data.  The "IS_SUCCESSFUl" column is the target variable because the model is attempting to predict whether the organizations will be successful.  The remaining columns are features of the model.  

## Results:
* Deliverable 1: Pre-Processing
Prior to running the data through the neural network it needs to be processed.  Unnecessary fields like EIN and Name were dropped.  Additionally, the unique values of each column were tabulated.

![unique val](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/unique%20values.png)

After the unique values were binned, the binned results were replaced in the data frame, and it the data frame was encoded prior to running it through the model. 

![encode table](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/encode%20table.png)

* Deliverable 2: Process Data Through the Model

The original model is comprised of 2 hidden layers with the first layer containing 80 neurons and the second layer containing 30 neurons.  The result of this model is not optimal since it only obtained a 72.7% accuracy rate and data loss of about 55.4%.

![first run](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/original%20results.png)

* Deliverable 3: Optimize the Model

Various steps were attempted to optimize the results.  Including additional processing of the underlying data.  A decision to bin the "INCOME_AMT" column seemed logical since it has 9 unique values.  

![bin income 1](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/bin%20income%20amount%201.png)

The data was processed consistent with the steps described above, which includes replacing the column values with the binned values and encoding the columns.  Three attempts to optimize the model were made.  Unfortunately, all three attempts presented results similar to the attempt described above.

![3 attempts](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/optimation%20results.png)

The first optimization attempt replaced the relu activation with tanH. The second attempt added additional layers to the model, and the third attempt additional neurons.   

## Summary:

Since the attempts described above have an accuracy rate of about 72%, the models in their current states are not desirable models to predict success.  As such, more work needs to be completed in order to use machine learning for prediction on this dataset.  It might be beneficial to conduct additional preprocessing of the data such as changing the bins.  Also, RFC are scalable so they work on a large datasets, . 
