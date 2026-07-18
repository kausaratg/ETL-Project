# Weather ETL Pipeline Using OpenWeather API

## Project Overview

This project demonstrates the implementation of a simple Extract, Transform, Load (ETL) pipeline using Python and the OpenWeather API. 
The pipeline retrieves real-time weather data for multiple cities, transforms the raw JSON response into a clean and structured dataset, 
and stores the processed data for future analysis.


## Data Source

**API:** OpenWeather Current Weather API

The data was collected through HTTP requests made to the OpenWeather API using a personal API key. 
The API provides real-time weather information, including temperature, humidity, wind speed, weather conditions, 
and other meteorological measurements.


## Technologies Used
* Python
* Requests
* Pandas
* Jupyter Notebook / VS Code
* OpenWeather API


## Project Structure

```text
weather-etl-pipeline/
│
├── data/
│   ├── weather_data.csv
│   ├── weather_data_cleaned.csv
│
├── notebooks/
│   └── weather_etl.ipynb
│
└── README.md
```


# ETL Process

## 1. Extract

The extraction phase involved connecting to the OpenWeather API using Python's `requests` library. 
Weather information was retrieved for **3** cities using authenticated API requests.

The following fields were extracted:

* City Name
* Temperature (°C)
* Humidity (%)
* Weather Condition
* Wind Speed (m/s)
* Date and Time of Extraction

The API returned the data in JSON format, which served as the raw dataset.


## 2. Transform

The extracted JSON data was transformed into a structured Pandas DataFrame.

Transformation steps included:

* Converting nested JSON objects into tabular columns
* Renaming columns for readability
* Converting the extraction timestamp to a datetime format
* Standardizing column names
* Validating data types
* Organizing the dataset into a clean format suitable for analysis

These transformations improved data consistency and prepared the dataset for downstream analysis.



## 3. Load

After transformation, the cleaned dataset was stored for future use CSV (`weather_summary_cleaned.csv`)


Storing the processed data ensures that it can be reused without repeatedly calling the API.


# Exploratory Analysis

Basic analysis was performed to compare weather metrics across the selected cities.

The analysis included:

* Comparing temperatures across cities
* Identifying the city with the highest temperature
* Identifying the city with the lowest temperature
* Determining the city with the highest humidity
* Comparing weather conditions
* Comparing wind speeds


# Key Findings

The analysis produced the following observations:

* **Temperature:** **Port Harcourt** recorded the highest temperature of **27.16°C**, while **Lagos** recorded the lowest at **24.56°C**.

* **Humidity:** The highest humidity level (**89%**) was observed in **Lagos**, whereas **Port Harcourt** had the lowest humidity (**72%**).

* **Weather Conditions:** The most common weather condition among the selected cities was **overcast clouds**. 

* **Wind Speed:** **Abuja** experienced the highest wind speed of **1.84m/s**, while **Lagos** recorded the lowest wind speed of **0.54m/s**.




