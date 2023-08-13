# Yearly Damage Costs of Natural Disasters
### Contributors: Benjamin Crane, Pu Gong, Bear Jordan, Ailun Li, Melirose Liwag

## Project Presentation
Click for a 12-minute presentation of the project:

[![GO TO video presentation](https://img.youtube.com/vi/odBVL16osb4/1.jpg)](https://www.youtube.com/watch?v=odBVL16osb4)

# Description
This project explores and compares the benefits of Bayesian Regression over OLS Regression in predicting the yearly cost of natural disasters. Building a reliable prediction model can help increase economic preparedness should a natural disaster occur. Specifically, this project tackles the effects of Hurricanes across the United States as our team found it was the most documented out of the common natural disasters in the US. 

Data used in this project:
1. [HURRICANE DATA] (https://www.kaggle.com/datasets/averyjackson/hurricaneinfo)
2. [HOUSING MARKET DATA] (https://redfin-public-data.s3.us-west-2.amazonaws.com/redfin_covid19/weekly_housing_market_data_most_recent.tsv000) for normalization

To get accurate and up-to-date predictions, we recommend downloading the latest data files 

# Documents
* Code: Contains data and code files to run the project
  1. [`HurricaneData.csv`](https://github.com/MeliroseLiwag/DamageCosts_NaturalDisasters/Hurricane-Project/Data/HurricaneData.csv) a simple version of the cleaned data
  2. [`Regression Analysis.Rmd`](https://github.com/MeliroseLiwag/DamageCosts_NaturalDisasters/Hurricane-Project/Notebooks/RegressionAnalysis.Rmd) the R notebook containing the analysis pipeline
  3. [`HurricaneDataEDA.ipynb`](https://github.com/MeliroseLiwag/DamageCosts_NaturalDisasters/Hurricane-Project/EDA/HurricaneDataEDA.ipynb) the Jupyter Notebook containing the EDA

# Installation
#### Requirements:
 - Alteryx
 - R version 4.1.2 or higher 
 - RStudio (or preferred R IDE)
 - Python 3.9 or higher
 - Python libraries: pandas, seaborn, matplotlib, numpy, folium
#### Data Pre-processing
Data pre-processing was done in the Alteryx program using the data sets stated above (Hurricane data and Housing market data). Our team decided to use Alteryx as it can be used to automate workflows for data cleaning and preparation. This program also allows us to save time in building up-to-date data sets for our models if needed.
#### Exploratory Data Analysis (EDA)
EDA of the Hurricane data can be viewed by opening [`HurricaneDataEDA.ipynb`](https://github.com/MeliroseLiwag/DamageCosts_NaturalDisasters/Hurricane-Project/EDA/HurricaneDataEDA.ipynb) directly on GitHub
1. Noticed an increasing trend of hurricane events (although data for years 2010-2020 is incomplete as of July 2022)
<img witdh="887" alt="hurricane event trends" src="https://github.com/MeliroseLiwag/DamageCosts_NaturalDisasters/Hurricane Project/Images/EDA03.png"> 
