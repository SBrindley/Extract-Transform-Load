# Project #2: Extract, Transform, and Load


![.jpg](README_Files/dataset-cover.png)


## Contents

* [Project Proposal](#Project-header)
* [Aims of the Project](#Aim-header)
* [Sources of Data](#Sources-header)
* [Required Setup](#Required-header) 
* [Data Transformation](#Transform-header)
* [Data Loading](#Data-Loading)
* [Collaborators](#Collaborators-header)


## <a id="Project-header"></a>Project Proposal
We decided to look at two datasets for YouTube viewing statistics in the UK with a view for creating and cleaning two tables to make a database ready for usage in PostGres. The Dataset we chose contained the top trending videos on the platform in Great Britain. The csv contained all the data for the videos and the JSON contained a reference to the category ID in the CSV file that could be used to categorise the data by video type.


## <a id="Aim-header"></a>Aims of the Project


Our Aim is to demonstrate how we can select a csv/json file, load the files into Jupyter Notebook to clean and prepare the data and to import into PgAdmin to create a competent Database.


## <a id="Sources-header"></a>Sources of the Data

We used a CSV and JSON file from Kaggle linked below. We also have a copy of the raw data in the resources/datasource folder in this repository.

https://www.kaggle.com/datasets/datasnaek/youtube-new


## <a id="Required-header"></a>Required Setup

To run the notebook.ipynb file you will need to install the following packages/dependencies:
* SQLAlchemy `pip install SQLAlchemy`
* Psycopg2 `pip install psycopg2`


To connect to the PostgreSQL database you will need to add your PgAdmin 4 username and password to a config.py file
![config_file.png](Readme_Images/config_file.png)
The config.py file should be stored in your local repository folder.


## <a id="Data-header"></a>Data Transformation

Our first steps after inspecting the data were to load them into Jupyter Notebook, the first file we looked at was the JSON file. 
We imported the relevant libraries screenshotted below:

![image](https://user-images.githubusercontent.com/113051302/214705228-7360ac0d-8527-44b8-b281-523966823275.png)

We checked the categories and needed to clean the items column and extract the category_id and category_name fields into dictionaries to then convert into a DataFrame

<img width="959" alt="image" src="https://user-images.githubusercontent.com/113051302/214705937-16d91309-a7d3-48ad-bcb0-1cefd3c693fa.png">

Next was the extraction and transformation of the bigger csv file. We extracted the relevant columns that we felt were relevant to the Database and converted it into a DataFrame.

After inspecting the DataFrame we decided to drop the publish_time, trending_date, thumbnail_link and some of the other columns we rendered unimportant.

<img width="953" alt="image" src="https://user-images.githubusercontent.com/113051302/214706595-d19ba0b0-8540-48a4-922f-cc6bedead719.png">

Once this was completed we could assess to see if any columns needed further transformation ready for the database. We replaced the separator in the tags and title columns was a pipeline symbol so we replaced this with a comma.

<img width="964" alt="image" src="https://user-images.githubusercontent.com/113051302/214707021-79975abd-70b0-4bd7-be80-8a6c12fd0258.png">

Our next step was to check the keys existed in both dataframes to ensure connection. When doing this we realised we needed to drop a category_id that was only present in the csv dataframe and therefore had no link to the JSON file and could not be categorised by category_id for our database. We dropped this and then moved on to check for duplication.

<img width="980" alt="image" src="https://user-images.githubusercontent.com/113051302/214708187-9987d4c5-b9d8-408e-b11c-a2fa60c261cd.png">





## <a id="Data-Loading"></a>Data Loading


## <a id="Collaborators-header"></a>Collaborators


Stanley, Olive, Siobhan and Jade


