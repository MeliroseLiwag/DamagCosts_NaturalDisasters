************************************************************************
██████╗ ███████╗ █████╗ ██████╗     ███╗   ███╗███████╗
██╔══██╗██╔════╝██╔══██╗██╔══██╗    ████╗ ████║██╔════╝
██████╔╝█████╗  ███████║██║  ██║    ██╔████╔██║█████╗  
██╔══██╗██╔══╝  ██╔══██║██║  ██║    ██║╚██╔╝██║██╔══╝  
██║  ██║███████╗██║  ██║██████╔╝    ██║ ╚═╝ ██║███████╗
╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝╚═════╝     ╚═╝     ╚═╝╚══════╝
                                                                                                     
************************************************************************

DESCRIPTION:
This is documentation for Team 25's course project. In the zip file containing this text, you will find the 
following two folders: 

    * DOC: Contains Team 25's project documentation.
        1. team025report.pdf--The final report for the project.
        2. Team025slides.pdf--The slide presentation for the project.

    * CODE: Contains data and code files to run the project.
        1. Natural Disaster Analysis.yxmd--the Alteryx data cleaning pipeline file. 
        2. HurricaneData.csv--a sample version of the cleaned data
        3. Regression Analysis.Rmd--the R notebook containing the analysis pipeline.
        4. HurricaneDataEDA.ipynb--the Jupyter Notebook containing the EDA.

INSTALLATION:
Unzip the contents of the CODE folder to a local folder of your choice. To run the data cleaning procedure, you will 
need access to Alteryx. The analysis can be run in RStudio or your preferred R IDE, provided R version 4.1.2 or 
higher is installed. A current copy of Anaconda3 will be needed to run the Jupyter Notebook. 

EXECUTION: 
To run just the Jupyter Notebook:
    - open the HurricaneDataEDA.ipynb file in Jupyter Notebook.

To run the analysis code also:
    - open Regression Analysis.Rmd in the R IDE.
    - make sure the file HurricaneData.csv is saved in the same folder containing the R notebook.
    - select "Run all code chunks" or equivalent in your IDE.

To run the data cleaning from scratch:
    - (if needed) Install Alteryx from https://www.alteryx.com/designer-trial/free-30-days
    - download the latest Flood data from https://www.fema.gov/openfema-data-page/fima-nfip-redacted-claims
    - download the latest Hurricane data from https://www.kaggle.com/datasets/averyjackson/hurricaneinfo
    - download the latest Redfin weekly data from
         https://redfin-public-data.s3.us-west-2.amazonaws.com/redfin_covid19/weekly_housing_market_data_most_recent.tsv000
         and save to the same folder.
         - IMPORTANT: rename the file to redfin_covid19/weekly_housing_market_data_most_recent.tsv (i.e., change the file extension to .tsv)
    - open Natural Disaster Analysis.yxmd in Alteryx and use the Directory menu to select the folder where the data files are saved.
    - click Run.

URL:
Final Video Presentation: https://www.youtube.com/watch?v=odBVL16osb4

