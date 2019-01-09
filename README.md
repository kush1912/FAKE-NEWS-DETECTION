# FAKE-NEWS-DETECTION
Machine learning Based Minor Project, which uses various classification Algorithms and NLP to classify the news into FAKE/REAL, on the basis of their Title and Body-Content. Data has been  collected from 3 different sources and uses algorithms like Random Forest, SVM, Wordtovec and Logistic Regression. It gave 94% accuracy overall, otherwise various comparisons are made from different classification algorithms used.

The Source code folder having below files
 Scrapping Data Folder
  - NYT_API_Key.txt -> NYT API Key file 
  - Guardian_API.txt -> Guradian API Key file
  - NYT.csv -> NYT dataset
  - Guardian.csv -> Guardian Dataset 
  - Scraping_NYT_data.ipynb -> code for scrapping data from New York Times 
  - Scraping_Guardian_Data.ipynb -> code for scrapping data from Guradians Post newws i.e Washington DC Newspaper
 
Cleaning data
  -Kaggle.ipynb -> code for cleaning Fake news data
  -Guardian_Cleaning.ipynb -> code for cleaning Guardian post data
  -NYT_Cleaning.ipynb -> code for cleaning New York Times data
 
Combining and Modeling
 - Combining and modeling.ipynb -> Code for implementation of models - Logistic regression, Random Forest and XGBoost
 

To execute the code,
First step is to scrape the data from NYT and guardians. Files to execute these are Scraping_NYT_data.ipynb and Scraping_Guardian_Data.ipynb
After scraping NYT data, we will get data into mongodb collection and export using mongoexport into NYT_DB.csv file.
After scraping data from Guradian post, we will get data in .json files.

Second step is to execute files in Cleaning data folder.
 - Execute Kaggle.ipynb to clean the fakenews data
 - Execute NYT_Cleaning.ipynb to clean New York Times data. Input to this code will be NYT_DB.csv file
 - Execute Guardian_Cleaning.ipynb to clean Guardians data. Input to this code should be set of all json files that we collected from Scraping_Guardian_Data.ipynb

After cleaning all the three data, we will get Kaggle_Clean.csv, NYT_clean.csv and Guardian_clean.csv files.

Third step is to execute file from Combining and Modeling folder.
 - Execute Combining and modeling.ipynb file for combining the three datasets and training the models.
 The combined datasets are in file Final.csv file. This csv file will be input for training the classifiers.

  
