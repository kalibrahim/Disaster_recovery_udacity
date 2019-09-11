# Disaster Response Pipeline Project

### Required Libraries:
- nltk 
- numpy 
- pandas 
- scikit-learn 
- sqlalchemy 

### Motivation:
This project is part of Udacity's Data Science Nanodegree. In this project I will provide a model that will classify disaster messages from data provided from Figure Eight.

This will include a web page that will provide a message classification based on the different message categories that is avaliable. A vizualization will also be included in the web page.


### Files:
* run.py
  * Flask file that runs the application as a web page. 
* process_data.py
  * This is a data cleaning pipeline.
    * Function:
      * Loads messages and category datasets
      * Merges the datasets based in ID
      * Cleans data
      * Stores in a database
* train_classifier.py
  * This is a machine learning pipeline.
    * Function:
      * Loads data from the database
      * Splits data into training and test datasets
      * Build a text processing and ML pipeline
      * Trains and tunes model based on GridSearchCV
      * Output test results
      * Export final model as pickle file

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl models/vocabulary_stats.pkl models/category_stats.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
