# Project #2: Extract, Transform, and Load


![.jpg](README_Files/dataset-cover.png)


## Contents

* [Project Proposal](#Project-header)
* [Aims of the Project](#Aims-of-the-Project)
* [Sources of Data](#Sources-of-the-Data)
* [Required Setup](#Required-header) 
* [Data Transformation](#Data-Transformation)
* [Data Loading](#Data-Loading)
* [Collaborators](#Collaborators-header)

## <a id="Project-header"></a>Project Proposal

We decided to look at two datasets for YouTube viewing statistics in the UK with a view for creating and cleaning two tables to make a database ready for usage in PostGres. The Dataset we chose contained the top trending videos on the platform in Great Britain. The csv contained all the data for the videos and the JSON contained a reference to the category ID in the CSV file that could be used to categorise the data by video type.



## <a id="Project-header"></a>Aims of the Project


Our Aim is to demonstrate how we can select a csv/json file, load the files into Jupyter Notebook to clean and prepare the data and to import into PgAdmin to create a competent Database.


## <a id="Project-header"></a>Sources of the Data

We used a CSV and JSON file from Kaggle linked below. We also have a copy of the raw data in the resources/datasource folder in this repository.

https://www.kaggle.com/datasets/datasnaek/youtube-new


## <a id="Required-header"></a>Required Setup

To run the notebook.ipynb file you will need to install the following packages/dependencies:
* SQLAlchemy `pip install SQLAlchemy`
* Psycopg2 `pip install psycopg2`


To connect to the PostgreSQL database you will need to add your PgAdmin 4 username and password to a config.py file
![config_file.png](Readme_Images/config_file.png)
The config.py file should be stored in your local repository folder.


## <a id="Project-header"></a>Data Transformation

Our first steps after inspecting the data were to load them into Jupyter Notebook, we started with the csv as this file had the larger amount of data in.

Once loaded in we transformed it into a DataFrame and then looked as dropping some of the columns we deemed irrelevant to the database we wanted to create.

After inspecting the DataFrame we decided to drop the publish_time, trending_date, thumbnail_link and some of the other columns we rendered unimportant.

Add a snapshot of the notebook here

** We then decided to make it cleaner by changing the column names


** Checked if there were duplicates




## <a id="Project-header"></a>Data Loading


## <a id="Collaborators-header"></a>Collaborators
Stanley, Olive, Siobhan and Jade


