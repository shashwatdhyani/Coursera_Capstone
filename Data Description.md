Data Description :

I have used the example Data set provided in the Capstone Project.
Data has the details on Accident occurrences in Seattle.
Data has been provided in the form of comma separated version (csv) file “Data-Collisions.csv” :

https://github.com/shashwatdhyani/Coursera_Capstone/blob/master/Data-Collisions.csv

The data file has 38 columns with SEVERITYCODE column repeating hence effectively 37 columns and 65691 rows.

We need to predict SEVERITYCODE hence SEVERITYCODE  is the Label/Target in the dataset.

However value count for SEVERITYCODE shows that data is not balanced and skewed towards Severity 1.
There are 45813 rows for Severity 1 and 18845 rows for Severity 2.

But since the data has been collated by the Seattle Traffic Department we can say the data is not biased.

If we drop the Severity 1 rows to balance the data then we will have to drop too many rows of data which could result in loss of information hence we did not drop any row for Severity 1 code.

Dataset has the details on the description and Severity of the Accidents happened on a particular day at a given Location and Junction. It has the details on the Weather condition , Light condition and the Road condition when the accident happened. It has record whether the vehicle was over speeding or not. It also has the details how many vehicles and people were involved or whether pedestrians were also involved. Data set also records kind of collision and whether the parked car was hit in the accident.
All these details have been recorded in the 37 columns (Features).

Not all features have been used to build the model.

We have taken the subset of all the columns (features) which would have more impact in predicting the Accident Severity . To find it we visualize the data , refer the metadata , apply statistical methods to narrow down on the columns we need to build the model.

'LOCATION','ADDRTYPE','COLLISIONTYPE','INATTENTIONIND','UNDERINFL','WEATHER','SPEEDING','LIGHTCOND','PEDROWNOTGRNT','ROADCOND','JUNCTIONTYPE','PERSONCOUNT','VEHCOUNT','HITPARKEDCAR'

Since this is the Supervised Classification problem we will convert the categorical data in Features into numerical data .
We will then split the data into Training data set and the Testing data set.
We will build the Model using the Training data set and evaluate the model using the Testing data set.
