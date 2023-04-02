# Neural Network Charity Analysis

## Overview:
The objective of this analysis is to utilize a neural network to forecast the success of Alphabet Soup's funded applicants.  

The [dataset](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/charity_data.csv) contains information on more than 34,000 organizations, and the analysis consists of three main steps. Firstly, the data is pre-processed, followed by the initial attempt to train a neural network with the data. Finally, various techniques are applied to optimize the model's accuracy. The target variable for this analysis is the "IS_SUCCESSFUL" column, as the model seeks to predict the success of funded organizations, while the remaining columns are utilized as features for the model.


## Results:
* [Deliverable 1](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/AlphabetSoupCharity.ipynb): Pre-Processing

Before feeding the data into the neural network, it needs to undergo processing. This involves dropping irrelevant fields like EIN and Name, and generating a table of the unique values present in each column.

<img src ="https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/unique%20values.png" width="600" height ="250"/>

Columns that had more than 10 unique values were binned, and the resulting bins replaced the original data frame before encoding it.. 

<img src ="https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/encode%20table.png" width="600" height ="250"/>

* [Deliverable 2](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/AlphabetSoupCharity.ipynb): Process Data Through the Model

The initial model consists of two hidden layers, where the first layer has 80 neurons and the second layer has 30 neurons. However, the model's performance is suboptimal, as it only achieves an accuracy rate of 72.7% and experiences a data loss of approximately 55.4%.

![first run](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/original%20results.png)

* [Deliverable 3](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/AlphabetSoupCharity_Optimzation.ipynb): Optimize the Model

In an effort to optimize the results, several steps were taken including additional processing of the underlying data. One decision was to bin the "INCOME_AMT" column due to its 9 unique values. 

![bin income 1](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/bin%20income%20amount%201.png)
The processed data, which includes binned values and encoded columns, was used in three attempts to optimize the model. However, all three attempts resulted in similar outcomes to the initial model described above.

<img src ="https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/3%20results.png" width="700" height ="400"/>

One attempt to optimize the model involved replacing the relu activation function with tanH. Another attempt involved adding more layers to the model, while a third attempt involved increasing the number of neurons in the layers. However, despite these efforts, the results remained similar to the original model with an accuracy rate of only 72.7% and a data loss of approximately 55.4%.

## Summary:

Given the low accuracy rate of about 72% for the optimization attempts described above, further work is required to develop a more effective machine learning model for predicting success on this dataset. Additional preprocessing steps may be necessary, such as modifying the bin sizes and removing certain columns from the analysis. Additionally, it may be worthwhile to explore alternative modeling techniques such as Random Forest Classifiers (RFCs). RFCs are suitable for large datasets, less susceptible to outliers, and are effective for binary classification tasks like the one presented in this analysis.
