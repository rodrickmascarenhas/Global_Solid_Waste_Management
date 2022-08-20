# Investigative Study and Predictive Analysis for Global Solid Waste Management

This research study intends to document Solid Waste Management System-related (SWMS) knowledge around the world with a focus in the U.S. and EU. The dataset contains data on socioeconomic contexts (S) for municipal sold waste generation (W3), management practices for solid wastes generated by the public sector (e.g., municipal solid waste (MSW), construction and demolition (C&D) debris, electronic wastes, disaster debris) etc. Additionally, we attempt to capture the socioeconomic contexts as well as performance metrics of SWMS, including economic benefits, environmental footprints, and societal impacts of the year 2015. This dataset contains implicit data obtained from multiple sources. For example, climate and temperature are values obtained from Köppen-Geiger classification of climate and temperature.


## Goals / Objectives

To determine whether a country has waste regulations from a dataset of 1720 records with several identifiers such as population, precipitation, temperature, land area, population density, household size, urbanization, expense, unemployment, age, energy, GDP, service, education index and sustainability index
<ul>
  <li>Create a model which may generate accurate results using the least number of features</li>
  <li>Provide insightful evidence on solid waste management</li>
  <li>Evaluating the predictive models using confusion matrix and accuracy score and determine the model with best accuracy score for analysis?</li>
  <li>Analyze the prediction using pre-determined test variables and draw results from the observations</li>
</ul>

Our desired goal will create actionable insights, uncover patterns and form hidden relationships from country demographics. The following are important questions we will answer during this project:

<ul>
  <li>Can these independent variables (features) be used to explain the target variable (waste regulation)?</li>
  <li>How do factors like household size, temperature, age, education index and sustainability index of a state/ territory determine their waste management practices?   </li>
  <li>What steps are necessary to improve on waste management activities?</li>
  <li>How can we plan resources for sustainability?</li>
</ul>


## Data Description

SWMS has 1720 instances, 18 descriptive attributes and the target variable of category type.

As observed in the following dataset abbreviations, these are the terminologies:

Feature	Description
Year	Year of the record
Population	Number of inhabitants of a country or a city
Climate	Köppen-Geiger classification of climate
Temperature	Köppen-Geiger classification of temperature
Population	Number of inhabitants of a country or a city
Land Area	Land area of a country or a city
Population Density	Number of inhabitants per square km
Household Size	Number of people per household
Urbanization	Percentage of people living in the cities
Expense	Percentage of GDP used for household and NPISHs consumption
Unemployment	Unemployment rate of a country
Age (15-64)	Percentage of population between age 15 & 64
Age (65+)	Percentage of population 65 & above
Energy	Per capita energy demand of a country
GDP	Per capita GDP of a country in constant 2015 USD
Service	Percentage of GDP from the service industry
Education	Education index of Human Development Index (HDI)
Sustainability	Sustainability index of a country
Regulation	Country has waste regulation or not

<ul>
  <li>The dataset contains no missing values and NAs but there were outliers that had to be removed</li>
  <li>Min-max transformation to the numerical variables resulted in lower accuracy, it was taken out</li>
  <li>Categorical data were converted to discrete values and dummy variables were created; reference values were discarded</li>
  <li>Continuous numerical data were checked for outliers. Columns were renamed accordingly</li>
</ul>


## Proposed Model and Justification

<ul>
  <li>Classifier will provide accurate readings as the target variable contains two factors (Yes or No) which means data is dichotomous</li>
  <li>We do not have the likelihood of finding a third target variable as the data suggests</li>
  <li>We assume that relationship between independent and dependent variables is non-linear and multi-linear regression won’t work</li>
  <li>It is difficult to translate qualitative to quantitative variables. Hence, we use classification predictive modelling</li>
</ul>

Our analysis can be divided into the following steps:

<ul>
  <li>Datasets must be split into training and testing subsets of data with each having their own independent and dependent variables</li>
  <li>We fit the training set with the following classification techniques: Logistic Regression, Decision Tree, Random Forest, Support Vector Machines (Linear),         Support Vector Machines (RBF), Boosting classifiers, K-Nearest Network, Artificial Neural Network, Naive Bayes</li>
  <li>Our classifier should evaluate multiple accuracy scores in pursuit of the highest accuracy score</li>
  <li>That model will be used to predict the target values for our out-of-sample dataset</li>
</ul>


## Result Implications

<ul>
  <li>The model appears valid and uses the common parameters to fit the target variable accurately. It then performs the testing predictions with good accuracy</li>
  <li>Model cannot tolerate missing values and sensitive to outliers, does not work well on imbalanced data</li>
  <li>Our best model KNN uses k=3 as the number of training examples needed to predict a new test example and prob=TRUE to return proportion of votes for the winning     class as attributes</li>
  <li>The results show training accuracy score is higher than testing accuracy score, selected model may lead to overfitting</li>
</ul>

Classifier can predict the outcome of our testing set with accuracy score of 96%. The score is adequate to determine the class of out-of-sample dataset. As the accuracy score is high, some or all the independent variables can be used to identify whether a particular municipal waste generator is regulated or not.

Factors such as “Education Index”, “Household Size”, “Temperature” and “Sustainability Index” can influence the regular practices of waste management. Waste management awareness plays an important role in waste collection and segregation. Places where Education index is high, waste regulation is prevalent.

Using out-of-sample data obtained from the year 2015, we see that our model can predict with an accuracy score of <b>96.5%</b>. This shows that there is less variance between training and out-of-sample scores.


## Concluding Remarks

<b>Prediction: We can predict with high accuracy the actual values of our data for the year 2015</b>
<b>Outlier data: The dataset contains outliers and missing/ NA values</b>
<b>Incosistent results: The model has better training set prediction accuracy than that of out-of-sample data, may lead to overfitting</b>
<b>Validation data: Predicting new data will result in lower accuracy score with increasing variability</b>
