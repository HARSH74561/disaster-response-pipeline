Disaster Response Pipeline Project
Table of Contents
Overview

Project Structure

Setup Instructions

How to Use

Credits

Application Snapshots

Overview
This project is a part of the Udacity Data Scientist Nanodegree, developed in collaboration with Figure Eight. The objective is to build a machine learning pipeline that classifies real-time messages received during natural disasters. This enables emergency response teams to quickly identify and prioritize aid based on message content.

The solution also includes a web interface where end users (e.g., responders or coordinators) can enter a message and receive its classification across multiple emergency-related categories.

Project Structure
The repository is organized into three key directories:

1. app/
run.py: Launches the Flask web app.

templates/: Contains the HTML files (master.html and go.html) for rendering the web interface.

2. data/
disaster_messages.csv: Raw messages dataset.

disaster_categories.csv: Category labels for messages.

process_data.py: Script to clean and transform the raw data, saving it to an SQLite database.

ETL Pipeline Preparation.ipynb: Jupyter Notebook outlining the data preprocessing steps.

DisasterResponse.db: The resulting SQLite database after preprocessing.

3. models/
train_classifier.py: Builds and trains a multi-output classification model, then saves it as a pickle file.

classifier.pkl: The trained model file used by the web app.

ML Pipeline Preparation.ipynb: Notebook containing initial model exploration and experimentation.

Setup Instructions
This project has minimal requirements and should work smoothly with any standard Anaconda Python distribution (Python ≥3.5).

To get started:
Run the data pipeline:
python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db

Train the machine learning model:
python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl

Launch the web application:
Navigate into the app/ folder and run:
python run.py


View the app:
Open your browser and go to http://0.0.0.0:3001/

How to Use
Once the application is running:

You'll see a dashboard showing visual summaries of the dataset.

Enter any message in the input box and click "Classify Message".

The application will output the categories the message belongs to, with active classifications highlighted.

Application Snapshots
Homepage with dataset insights


Message classification input


Classification output


Data pipeline execution


Training the classifier


Starting the web server


