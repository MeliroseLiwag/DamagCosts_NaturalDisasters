# Yearly Damage Costs of Natural Disasters
### Contributors: Benjamin Crane, Pu Gong, Bear Jordan, Ailun Li, Melirose Liwag

## Project Presentation
Click for a 12-minute presentation of the project:

[![GO TO video presentation](https://img.youtube.com/vi/odBVL16osb4/1.jpg)](https://www.youtube.com/watch?v=odBVL16osb4)

# Description
This project explores the benefits of Bayesian Regression and OLS Regression in predicting the yearly cost of natural disasters. Building a reliable prediction model can help increase economic preparedness should a natural disaster occur. Specifically, this project tackles the effects of Floods and Hurricanes across the United States as our team found they were the most documented out of the common natural disasters in the US. 

Data used in this project:
1. [HURRICANE DATA] (https://www.kaggle.com/datasets/averyjackson/hurricaneinfo)
2. [FLOOD DATA] (https://www.fema.gov/openfema-data-page/fima-nfip-redacted-claims)
3. [HOUSING MARKET DATA] (https://redfin-public-data.s3.us-west-2.amazonaws.com/redfin_covid19/weekly_housing_market_data_most_recent.tsv000) for normalization and calculate claims per state

To get accurate and up-to-date predictions, we recommend downloading the latest data files 

# Documents
* Code: Contains data and code files to run the project
  1. [`HurricaneData.csv`](/Hurricane%20Project/Data/HurricaneData.csv) a simple version of the cleaned data
  2. [`Regression Analysis.Rmd`](/Hurricane%20Project/Notebooks/Regression%20Analysis.Rmd) the R notebook containing the analysis pipeline
  3. [`HurricaneDataEDA.ipynb`](/Hurricane%20Project/EDA/HurricaneDataEDA.ipynb) the Jupyter Notebook containing the EDA

# Analysis
#### Requirements:
 - Alteryx
 - R version 4.1.2 or higher 
 - Python 3.9 or higher
 - Python libraries: pandas, seaborn, matplotlib, numpy, folium
#### Data Pre-processing
Data pre-processing was done in the Alteryx program using the data sets stated above (Hurricane data and Housing market data). Our team decided to use Alteryx as it can be used to automate workflows for data cleaning and preparation. This program also allows us to save time in building up-to-date data sets for our models if needed.
![Alteryx Pipeline](/Hurricane%20Project/Images/Alteryx.png)
#### Exploratory Data Analysis (EDA)
EDA of the Hurricane data can be viewed by opening [`HurricaneDataEDA.ipynb`](/Hurricane%20Project/EDA/HurricaneDataEDA.ipynb) directly on GitHub
1. Notice an increasing trend of hurricane events (although data for years 2010-2020 is incomplete as of July 2022)

![Hurricane Event Trends](/Hurricane%20Project/Images/EDA03.PNG)

2. These variables are highly correlated: "Year" and "Decade", "Pressure" and "WindSpeed", and "Year" and "WealthPerCap"
   - "Year" is also correlated with "Damage" and indicates that inflation might be an additional factor
   - "Population" has low to no correlation to any factor
  
  ![Correlation Matrix](/Hurricane%20Project/Images/EDA04.PNG)

The data was later adjusted by normalizing costs per year with a 'Table of Historical Inflation Rates in Percent' data set for 1914 to 2022. As mentioned, our models can be updated with up-to-date datasets through Alteryx if need be.
#### Models - Bayesian Regression
Analysis can be found in [`Regression%20Analysis.Rmd`](/Hurricane%20Project/Notebooks/Regression%20Analysis.Rmd)

We found that the data can be explained with the variables "Area", "WealthPerCap" and "Population." Model assumptions show that the model is a good fit and that the model should be statistically reliable.

![Model Assumptions](/Hurricane%20Project/Images/Bayesian_assumptions.png)
#### Models - OLS Regression
Analysis can be found in [`Regression%20Analysis.Rmd`](/Hurricane%20Project/Notebooks/Regression%20Analysis.Rmd)
Model assumptions also show that this model is a good fit and should be statistically reliable. The response variable is log-transformed due to heteroscedasticity.

![Model Assumptions](/Hurricane%20Project/Images/OLS_assumptions.png)

# Hypotheses
#### We expect to see an increasing variability in the year-to-year error component
In this time series analysis, we observed an increasing trend in damage costs through the decades so we failed to reject this hypothesis

![Variability per Year](Hurricane%20Project/Images/TimeSeries.PNG)

#### We expected to see an increasing trend in the magnitude of disaster-related parameters over time.
Parameters observed: 
  - Wind Speed at landfall
  - Pressure near landfall
  - Area of Total Destruction

In this time series analysis, we observed a decreasing trend over time and although there is a small spike in one of the graphs, the spike is still less than how it was in the 1900s. With this, we reject this hypothesis.
![Wind Speed at landfall](/Hurricane%20Project/Images/WindSpeed.PNG) ![Pressure near landfall](/Hurricane%20Project/Images/Pressure.PNG) ![Area of Total Destruction](/Hurricane%20Project/Images/ATD.PNG)

#### We expected the Bayesian regression model to outperform the OLS regression model in terms of predictive power and interpretability
We found that there cannot be a direct comparison between the 2 models as each model has its own added benefits. Although the Bayesian regression model has better predictive power, posterior analysis of the Bayesian model is harder to interpret if one is unfamiliar with said model. With this, we will reject this hypothesis.

![OLS intervals](/Hurricane%20Project/Images/Conf_Pred_Int.PNG) ![Bayesian Prediction](/Hurricane%20Project/Images/Bayesian_Prediction.png)
