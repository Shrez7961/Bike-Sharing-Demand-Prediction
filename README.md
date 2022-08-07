![](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimg.caixin.com%2F2017-05-22%2F1495449722173744.jpg&f=1&nofb=1)
# Problem Statement
The dataset contains weather information
(Temperature, Humidity, Windspeed,
Visibility, Dewpoint, Solar radiation, Snowfall,
Rainfall), the number of bikes rented per hour,
and date information.
Based on the given data we have to build a
machine learning model which will be helping
us to predict the number of bikes that must be
made available by predicting the demand for
bikes rented per day.

# Introduction
Currently, the bike-sharing scheme is
well-received throughout the world. It
is a shared bike service for individuals,
which is free of charge and for a short-
term basis at a minimal rate. Most bike-
sharing systems permit people to
borrow and return a bike from a bike
station to another station that belongs to
the same network. Bike-sharing gains a
vast range of attention in recent years as
part of initiatives to boost the use of
cycles, improve the first mile/last mile link to other modes of transportation,
and minimize the negative effect of
transport activities on the environment.
Bike-sharing has significant impacts on
establishing a larger cycling
community, increasing the use of
transportation, minimizing greenhouse
gas emissions, enhancing public health,
and also traffic troubles.

# Objective
To predict the bike demands for the next day based on certain conditions like weather forecasting, holidays and active users in particular areas by analysing the previous data.
# Exploratory Data Analysis
Exploratory Data Analysis (EDA) plays a vital
role in the analysis of the data variables which
are important from the aspect of feature
engineering. It will help us to distribute and
relate between dependent and independent
variables. We have gone through an analysis of
every independent as well as the dependent
variable to check which independent factor
affects the dependent factor.

# Correlation Analysis
The correlation analysis has been done
to get a better understanding of dependent and
independent variables’ multicollinearity.
Multicollinearity may not affect the accuracy
of the model as much but we might lose
reliability in determining the effects of
individual independent features on the
dependent feature in your model and that can
be a problem when we want to interpret your
model.

# Feature Engineering
## One Hot Encoding of categorical feature:
One hot encoding is useful for data that has no relationship to each other. Machine learning algorithms treat the order of numbers as an attribute of significance. In other words, they will read a higher number as better or more important than a lower number.

While this is helpful for some ordinal situations, some input data does not have any ranking for category values, and this can lead to issues with predictions and poor performance. That’s when one hot encoding saves the day.

One hot encoding makes our training data more useful and expressive, and it can be rescaled easily. By using numeric values, we more easily determine a probability for our values. In particular, one hot encoding is used for our output values, since it provides more nuanced predictions than single labels.
## Ordinal Encoding:
In ordinal encoding, each unique category value is assigned an integer value.

For example, “red” is 1, “green” is 2, and “blue” is 3.

This is called an ordinal encoding or an integer encoding and is easily reversible. Often, integer values starting at zero are used.

For some variables, an ordinal encoding may be enough. The integer values have a natural ordered relationship between each other and machine learning algorithms may be able to understand and harness this relationship.

# Building Machine Learning Algorithm
The machine learning models used are as follows:
## Logistic Regression
Logistic regression is a classification technique that predicts the likelihood of a single-valued result (i.e. a dichotomy). A logistic regression yields a logistic curve with values only ranging from 0 to 1. The likelihood that each input belongs to a specific category is modelled using logistic regression. Logistic regression is a fantastic tool to have in your toolbox for classification purposes.
## Decision Tree

A decision tree is a supervised learning technique used to solve categorization problems. Both categorical and continuous input and output variables are supported.
## Random Forest
We create several trees in the Random Forest model rather than a single tree in the CART model. From the subsets of the original dataset, we create trees. These subsets can contain a small number of columns and rows. Each tree assigns a categorization to a new object based on attributes, and we say that the tree "votes" for that class. The classification with the highest votes is chosen by the forest

# Conclusion:
After applying linear regression model, we got R2 score of 0.779 for training data and R2 score of 0.774 for test data, which
signifies that model is optimally fit on both training and test data i.e. no overfitting is seen.
• Therefore, for even better fit, we applied polynomial regression model with degree = 2, we got R2 score of 0.933 for training
data and 0.90 for test data
• We also tried Tree based classifiers for our data, we applied Decision Tree Regressor, since decision tree is prone to overfit,
we gave certain parameters like maximum depth of the tree, maximum leaf nodes etc, with that we we got R2 score of 0.835 for
training data and 0.803 for test data which is less than polynomial regression.
• To get better accuracy on tree based model, we applied Random forest with n_estimator as 180 and with maximum depth as
13, with that we got R2 score of 0.888 for training data and 0.875 for test data.
• Finally, we applied Gradient boost with parameters selected after grid search which resulted in highest R2 score of 0.958 for
training data and 0.933 for test data with very less mean squared error of 6 and 10 in training as well as in test data.
• Also we can see from SHAP summary that high Hour_18 value increasing prediction. Also we can see low Snowfall value
increasing prediction and it is a common phenomenon in all the models.
• Lastly, In bar graph from SHAP we can see Winter has the highest feature value while Wind Speed has the Lowest shap
value.We can conclude that Hour_21,Hour_8 and Wind Speed is not contributing in Decision Tree,Random Forest and
Gradient Boost in model prediction.
