# Hacklytics2021

## Inspiration
The Covid-19 Pandemic has changed almost all aspects of our lives - but it has had perhaps the greatest effect on mobility. Most Covid-19 policies restrict human mobility, intending to reduce close-proximity contacts, the major driver of the disease’s spread. However, movement hasn’t completely stopped - some people still have to travel to work, people visit the park or have to make essential trips to the grocery store - and Covid-19 has continued to spread. This lead us to wanting to investigate the relationship between Covid-19 and mobility, which led us to the question, can we predict future COVID-19 cases based on present mobility?

## How we built it
Our work was done on Jupyter Notebook, and we used Python and the numpy, pandas, matplotlib and scikit libraries.

1) Data Gathering and Preprocessing After considering multiple data sets, we narrowed it down to Google Mobility Data (https://www.google.com/covid19/mobility/) and Covid case data from Kaggle (https://www.kaggle.com/johnjdavisiv/us-counties-covid19-weather-sociohealth-data)

Next, we had to convert the data into manageable data. We decided to limit our data to counties with enough mobility data and bucketed data by weeks to remove in-weekly fluctuations.

2) Time Series Analysis We used time-lagged cross correlation to see if there is any leader-follower relationship between time-series. We found that cases were inversely correlated with mobility except residential mobility, as expected, however, there was inconclusive evidence on mobility affecting cases.

3) Model Development The target variable for our model is new Covid-19 cases and number of deaths in the following time period [t, t+1]. As we are predicting more than one target variable we have used Multi-output regression In multi-output regression, typically the outputs are dependent upon the input and upon each other. Our multi-output regressor that predicts the number of covid cases and number of deaths in the time period [t,t+1] based on the past covid data and the mobility data.

Results: When predicting Covid cases/deaths one week in the future, our model has an accuracy of 90.6%. When predicting cases/deaths three weeks in the future, our model has an accuracy of 81.3% (when mobility is not considered, the accuracy is 74.9% - a significant increase, indicating mobility has an effect)

## **The notebook main-dash is an updated version of main-copy with visualiztions using plotly **

## Links
Devpost: https://devpost.com/software/investigating-the-relationship
