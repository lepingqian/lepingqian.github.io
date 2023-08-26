---
layout: post
title:  Data Analytics Competition Winning Entries
date:   2020-12-01 16:03:00 +0300
image:  06.jpg
tags:   Data_Analytics
---
## Data Analytics Competition Final Project

### Requirements and Evaluation
1. Participants are required to thoroughly read the case introduction, fulfill the basic requirements, and are encouraged to go beyond the basics by incorporating additional analysis.
2. Participants in the Python Data Analysis category and the Excel Data Analysis category should use respective tools to complete the case requirements. The analysis report should be crafted using Microsoft Word, with a focus on incorporating both graphics and text.
3. The judging panel will evaluate the submitted analysis reports based on content (completeness of the project, data visualization, innovation, etc.) and presentation (format, layout, etc.).

### Project Introduction

#### Dataset Name: Taipei Real Estate Dataset.xlsx

#### Dataset Overview

The Taipei Real Estate dataset comprises property information from Xindian District, New Taipei City. The dataset is in xlsx format, containing a total of 414 records. "NA" denotes missing data. It includes 6 explanatory variables:

X1 = Transaction Year-Month (e.g., 2013.250 represents March 2013, 2013.500 represents June 2013, and so on)

X2 = Age of the Property (in years)

X3 = Distance to the Nearest Bus Stop (in meters)

X4 = Number of Nearby Convenience Stores (integer)

X5 = Geographic Latitude Coordinates (in degrees)

X6 = Geographic Longitude Coordinates (in degrees)

The response variable:
Y = Unit Area Price (price per ping, measured in New Taiwan Dollars, where 1 ping = 3.3 square meters)

### Outline of Analysis Report

Project overview, analysis objectives, summary of methods used, results analysis, conclusions, etc. The analysis report must include the basic requirements, while participants are encouraged to add their own analysis content beyond the basics.

### Data cleaning

####Analyzing the Basic Structure of the Dataset

Querying and Outputting the First 5 and Last 5 Rows of Data

First 5 Rows:

![]({{site.baseurl}}/img/16.jpg)

Last 5 Rows:

![]({{site.baseurl}}/img/17.jpg)

Identifies and outputs the types of all feature in the dataset:

![]({{site.baseurl}}/img/18.jpg)

#### Missing Values 
1. Mean imputation
![]({{site.baseurl}}/img/19.jpg)
2. Median imputation
![]({{site.baseurl}}/img/20.jpg)
3. Mode imputation
![]({{site.baseurl}}/img/21.jpg)
4. Forward fill
![]({{site.baseurl}}/img/22.jpg)
5. Backward fill
![]({{site.baseurl}}/img/23.jpg)
6. Pandas linear interpolation
![]({{site.baseurl}}/img/24.jpg)

#### Outliers

Viewing data outliers:
![]({{site.baseurl}}/img/25.jpg)

Next, conducting an initial visualization of the correlation within the structured data.

![]({{site.baseurl}}/img/27.jpg)

![]({{site.baseurl}}/img/28.jpg)

#### Data standardization

Utilizing the StandardScaler() method from sklearn to perform standardization on the data, resulting in data with a mean of 0 and a variance of 1 after processing.
![]({{site.baseurl}}/img/26.jpg)

#### Constructing the model after splitting the data using K-fold Cross Validation

![]({{site.baseurl}}/img/29.jpg)
![]({{site.baseurl}}/img/30.jpg)
![]({{site.baseurl}}/img/31.jpg)
![]({{site.baseurl}}/img/32.jpg)
![]({{site.baseurl}}/img/33.jpg)
![]({{site.baseurl}}/img/34.jpg)

#### Analyzing Model Accuracy
![]({{site.baseurl}}/img/35.jpg)
![]({{site.baseurl}}/img/36.jpg)
![]({{site.baseurl}}/img/37.jpg)
![]({{site.baseurl}}/img/38.jpg)
![]({{site.baseurl}}/img/39.jpg)
![]({{site.baseurl}}/img/40.jpg)
![]({{site.baseurl}}/img/41.jpg)
![]({{site.baseurl}}/img/42.jpg)
![]({{site.baseurl}}/img/43.jpg)

#### Error Analysis and Model Parameter Testing
![]({{site.baseurl}}/img/44.jpg)
![]({{site.baseurl}}/img/45.jpg)
![]({{site.baseurl}}/img/46.jpg)
![]({{site.baseurl}}/img/47.jpg)
![]({{site.baseurl}}/img/48.jpg)


#### Model Evaluation
![]({{site.baseurl}}/img/49.jpg)
![]({{site.baseurl}}/img/50.jpg)

Results Analysis:

By comparing the results of various models including Linear Regression, Linear Regression after dropping features using VIF, Ridge Regression, Lasso Regression, Bayesian Ridge Regression, Random Forest Regressor, Linear Regression VIF, Random Forest Regressor VIF, and Random Forest Regressor RFE, a comparison was conducted using two-dimensional tables and bar charts depicting the outcomes of each model. It was observed that the Random Forest Regressor RFE exhibited the most favorable performance.
