# Disaster Response Pipeline Project
![Intro Picture](app/static/Disaster_Project.png)

## Table of Contents
1. [Installation](#installation)
	1. [Instructions](#instructions)
2. [Project Motivation](#project-motivation)
3. [File Descriptions](#file-descriptions)
	1. [File Structure](#file-structure)
4. [Results](#results)
5. [Licensing, Authors, Acknoledgements](#licensing-authors-acknowledgements)

## Installation
git clone the repository
```
https://github.com/linnforsman/disaster-response-pipeline.git
```
### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.
 - To run ETL pipeline that cleans data and stores in database: `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`

 - To run ML pipeline that trains classifier and saves: `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app: `python run.py`

3. Go to http://0.0.0.0:3001/

## Project Motivation
This project is part of the Data Scientist Nanodegree by Udacity in collaboration with Figure Eight. The dataset contains pre-labelled tweet and messages from real-life disaster events. The project aim is to build a Natural Language Processing model to categorize messages on a real time basis.
## File Descriptions
1. ``data/process_data.py``: This file contains the ETL pipeline that processes the raw data and stores it in the database.
2. ``models/train_classifier.py``: This file contains the ML pipeline that trains the classifier and saves it to the database.
3. ``app/templates/*.html``: This directory contains the html templates for the web app.
4. ``run.py``: This file contains the flask app that runs the web app.
### File Structure
``` 
app
| - template
| |- master.html # main page of web app
| |- go.html # classification result page of web app
|- run.py # Flask file that runs app
data
|- disaster_categories.csv # data to process
|- disaster_messages.csv # data to process
|- process_data.py
|- InsertDatabaseName.db # database to save clean data to
models
|- train_classifier.py
|- classifier.pkl # saved model
README.md

```

## Results
1. This is an example of a message we can type to test the performance of the model.
![Disaster Response Pipeline](app/static/Disaster_R_Project_test1.png)
2. After clicking Classify Message, we can see the categories which the message belongs to highlighted in green.
![Disaster Response Pipeline](app/static/Result_Disaster_2.png)
## Licensing, Authors Acknowledgements
The data was provided by [Figure Eight](https://appen.com) in collaboration with [Udacity]().