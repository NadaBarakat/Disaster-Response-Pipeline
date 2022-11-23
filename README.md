# Disaster Response Pipeline Project
#### File Structure

- app<br>
| - template<br>
| |- master.html  # main page of web app<br>
| |- go.html  # classification result page of web app<br>
|- run.py  # Flask file that runs app<br>

- data<br>
|- disaster_categories.csv  # data to process<br> 
|- disaster_messages.csv  # data to process<br>
|- process_data.py<br>
|- CleanDatabase.db   # database to save clean data to<br>

- models<br>
|- train_classifier.py<br>
|- cv_AdaBoostr.pkl  # saved model <br>

- README.md<br>

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
        
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/cv_AdaBoost.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
