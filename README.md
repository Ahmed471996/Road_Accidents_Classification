# Car_Accident

## About the project 

In this project, you will employ several supervised algorithms to accurately model Casualty Severity using data collected from Leeds City - UK for 2011. We will then choose the best candidate algorithm from preliminary results and further optimize this algorithm to best model the data.

We also will try to use data visualization and exploration to get some insights about the dataset.

Dataset Information
The data attached is about Car Accidents across Leeds City - UK for 2011. The outcome is to predict the variable which is Casualty Severity Data Description

Features

Reference Number

Easting

Northing

Number of Vehicles

Accident Date

Time (24hr)

1st Road Class :A roads – major roads intended to provide large-scale transport links within or between areas. B roads – roads intended to connect different areas, and to feed traffic between A roads and smaller roads on the network.

All UK roads (excluding motorways) fall into the following 4 categories:

A roads – major roads intended to provide large-scale transport links within or between areas B roads – roads intended to connect different areas, and to feed traffic between A roads and smaller roads on the network classified unnumbered – smaller roads intended to connect together unclassified roads with A and B roads, and often linking a housing estate or a village to the rest of the network. Similar to ‘minor roads’ on an Ordnance Survey map and sometimes known unofficially as C roads unclassified – local roads intended for local traffic. The vast majority (60%) of roads in the UK fall within this category

Road Surface

Lighting Conditions

Weather Conditions

Casualty Class

Sex of Casualty

Age of Casualty

Type of Vehicle

Casualty Severity


![image](https://user-images.githubusercontent.com/101316217/207074542-3fbde73b-9eaf-4eaf-865d-803349517bf3.png)

## Solutions Approaches 

### 1. First approach
We will deal with the label as multiclass classification

Which is the most important ?

we'll assume that recall is the most important in this problem so that we must not say it's not a fatal accident and it's actually a fatal accident (recall decreases as the false negative increases which gives us an indication of how good our model)

however we don't care much about precision as even if we say it's a fatal accident and we dicovered later that it's not it'll not be that harm to think about as a real world probelm.

### 2. Second approach
In this approach we'll assume the Fatal and Serious have the same importance so we'll consider them the same class and make the problem binary classification and deal with it as a fraud problem.

### Conclusion and Insights
In conclusion, data is imbalanced we dealt with it using many approaches such as oversampling and undersampling using Smote and random undersampling respectively and we used two approaches the first was to deal with the label as 3 classes, and with the help of oversampling and the random undersampling and 3 models we focused on the recall of the fatal or serious class as the recall of them is very important if we care about classifying with the minimum number of false negative (we classify the accident as not fatal or not serious and it's really not serious because if not people will die if we consider it as not fatal or not serious and not to do anything about it) and we can make a tradeoff and classify an accident sometimes as fatal but later we discover it wasn't but it's okay with that. We can also see the problem to care about precision somehow in order to minimize the false positives or the amount of effort or ambulances that will go to the accident place.

However we can deal with the problem as binary classification, so we can deal with it as fatal or not and consider fatal and serious the same also considering the recall of the fatal class as the most important.

We can also consider the precision of the not fatal class so that when we say this accident is not fatal will be accurate as possible.

## Future Work

We Can try different approaches to deal with the problem (working on precision or F-beta score)

