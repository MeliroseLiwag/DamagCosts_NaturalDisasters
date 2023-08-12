# Yearly Damage Costs of Natural Disasters
### Contributors: Benjamin Crane, Pu Gong, Bear Jordan, Ailun Li, Melirose Liwag

## Project Presentation
Click for a 12-minute presentation of the project:

[![GO TO video presentation](https://img.youtube.com/vi/odBVL16osb4/1.jpg)](https://www.youtube.com/watch?v=odBVL16osb4)

# Description
This project explores and compares the benefits of Bayesian Regression over OLS Regression in predicting the yearly cost of natural disasters. Building a reliable prediction model can help increase economic preparedness should a natural disaster occur. Specifically, this project tackles the effects of Floods and Hurricanes across the United States as our team found they were the most documented out of the common natural disasters in the US. 

Data used in this project:
1. [FLOOD DATA] (https://www.fema.gov/openfema-data-page/fima-nfip-redacted-claims)
2. [HURRICANE DATA] (https://www.kaggle.com/datasets/averyjackson/hurricaneinfo)
3. [HOUSING MARKET DATA] (https://redfin-public-data.s3.us-west-2.amazonaws.com/redfin_covid19/weekly_housing_market_data_most_recent.tsv000) for normalization

To get accurate and up-to-date predictions, we recommend downloading the latest data files 

# Documents
* Documents: Contains project Documentation
  1. [`team025report.pdf`] The Final report for the project
  2. [`Team025slides.pdf`] The slide presentation for the project
* Code: Contains data and code files to run the project
  1. [`Natural Disaster Analysis.yxmd`] the Alterys data cleaning pipeline file
  2. [`HurricaneData.csv`] a simple version of the cleaned data
  3. [`Regression Analysis.Rmd`] the R notebook containing the analysis pipeline
  4. [`HurricaneDataEDA.ipynb`] the Jupyter Notebook containing the EDA

 # Installation
 #### Requirements:
 - Alteryx
 - R version 4.1.2 or higher 
 - RStudio (or preferred R IDE)
 - Python 3.9 or higher
 - Python libraries: pandas, seaborn, matplotlib, numpy, folium

# Execution
EDA of the Hurricane data can be viewed by opening [`HurricaneDataEDA.ipynb`]
