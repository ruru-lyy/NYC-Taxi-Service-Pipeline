# NYC Taxi Service Pipeline and Dashboard

In this project, I will be showing you how I created a data pipeline from the New York City Taxi Service data (TLC Trip Record Data) utilizing tools such as Jupyter for an initial test code, Mage.ai for building the ETL pipeline, GCP for data storage and running BigQuery, and finally, loading the transformed data into Looker Studio for analytics. 

## About the Dataset 

### TLC Trip Record Data

In this dataset, Yellow and green taxi trip records include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts. 

__Note:__ The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC) by technology providers authorized under the Taxicab & Livery Passenger Enhancement Programs (TPEP/LPEP). The trip data was not created by the TLC, and TLC makes no representations as to the accuracy of these data.

You may access the dataset through the following link: https://storage.googleapis.com/taxi-service-data-engineering-niru/nyc_taxi_data.csv 

![Dataset](https://github.com/ruru-lyy/NYC-Taxi-Service-Pipeline/blob/main/data/data_screenshot.png)

For reference, we will be using the data dictionary that is available at: https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf which is also attached here-

![Data Dictionary](https://github.com/ruru-lyy/NYC-Taxi-Service-Pipeline/blob/main/data_dict.png)

### Technologies Used

__Programming Language:__ Python 3.9.19 (Jupyter Notebook)

__Cloud Services:__
1. Google Cloud Storage
2. Compute Engine Instance for mage to create an ETL pipeline
3. BigQuery
4. Looker Studio

__Data Pipeine Tool__ - https://www.mage.ai/

### Data Architecture

This shows the entire architecture of the project from data ingestion, data storage, ETL, querying and finally a basic interactive dashboard.

![Data Architecture](https://github.com/ruru-lyy/NYC-Taxi-Service-Pipeline/blob/main/nyc_taxi_data_architecture.png)

The process follows the following steps:

1. Data Ingestion and Storage: Obtain the data from nyc.gov and upload it onto Google Cloud Storage and set it to public access to obtain URL.
2. ETL Processing: Mage.ai extracts the data using the URL that was saved earlier, transformation code to perform data cleaning and data modeling (sometimes, data training when required) and afterwards, it is being loaded into BigQuery through Google Cloud API credentials.
3. Data Analysis and Querying: The transformed data is then loaded into BigQuery where SQL queries are run to obtain insights.
4. Data Visualization: Finally, Looker Studio is used to create a simple interactive dashboard and a report.

### Data Modeling 

Following is the data model that was referenced in the entire data engineering process-

![Data Modeling](https://github.com/ruru-lyy/NYC-Taxi-Service-Pipeline/blob/main/data/data_screenshot.png)

**Note:** Some of these columns like trip_distance or fare_amount may seem like measures but for learning purposes they are placed in dimension tables here. It’s all about making it easier to understand relationships in the data.

### 










