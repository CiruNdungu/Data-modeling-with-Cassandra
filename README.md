**DATA MODELING WITH CASSANDRA**

**OBJECTIVE**

The objective of this project is to create a NoSQL analytics database in Apache Cassandra for the startup, Sparkify. The analytics team in Sparkify seeks to understand what, when and how users are playing songs on the company's music streaming app. The analysts need an easy way to query and analyze the data, which is currently stored in raw csv files on a local directory.
As the projects data engineer, I have implemented an ETL pipeline in python to pre-process the data. The database tables are modeled on the queries according to the principle of one table per query. The primary and clustering keys for each table are selected to ensure a unique identifier for each row

**DATASETS**

The dataset is named event_data. The directory contains CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:
event_data/2018-11-08-events.csv
event_data/2018-11-09-events.csv

**ETL PIPELINE**

This project builds an ETL pipeline with Python to create the DB and the tables, fetch data from CSV files, process the data into one datafile (event_datafile_new.csv), load the data in Apache Cassandra and run the queries.
The new CSV titled event_datafile_new.csv contains the following columns:
•	artist
•	firstName of user
•	gender of user
•	item number in session
•	last name of user
•	length of the song
•	level (paid or free song)
•	location of the user
•	sessionId
•	song title
•	userId

The ETL pipeline for the project is in three steps:
1.	Extract: Process CSV files in the directory event_data to create a new CSV file, event_datafile_new.csv
2.	Transform: Create an Apache Cassandra database and load data from the new CSV file onto the tables.
3.	Load: Run the queries on database.

**ER DIAGRAM**


![ER diagram](https://user-images.githubusercontent.com/116004104/200495289-e667565f-601d-4e35-92cb-645a5bc52cfc.JPG)













**STRUCTURE**

1.	event_data folder containing the data.
2.	Project_1B_ Project_Template.ipynb the code.
3.	event_datafile_new.csv The CSV file that will be used to insert data into the Apache Cassandra tables.
4.	images a screenshot of what the denormalized data should look like in the event_datafile_new.csv.
5.	README.md project overview description

The project is launched by running the Project_1B_ Project_Template.ipynb to validate data loads and check the sample queries.

