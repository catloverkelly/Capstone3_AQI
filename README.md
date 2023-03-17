# Forecasting Monthly Median AQI Levels in the US
### Springboard Capstone 3 Project
Air Quality Index (AQI) is the primary to measure the current quality of the air. AQI values range from 0-500, with 0 being perfectly healthy, and 500 being extremely hazardous. However, values above 500 can occur -- these levels are called "Beyond the AQI". 

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="https://ww2.arb.ca.gov/sites/default/files/inline-images/2-air_quality_index_2.png">
 <source media="(prefers-color-scheme: light)" srcset="https://ww2.arb.ca.gov/sites/default/files/inline-images/2-air_quality_index_2.png">
 <img alt="YOUR-ALT-TEXT" src="https://ww2.arb.ca.gov/sites/default/files/inline-images/2-air_quality_index_2.png">
</picture>

Given daily AQI data from the US, can we forecast the monthly median AQI levels for the next year? Is there a trend in AQI? Moreover, are there correlations between AQI, and certain features such as latitude, longitude, or population density?

### The Dataset
The dataset is a table of AQI values from stations across the US from 1980-2022 acquired from kaggle.com. It contains 5.72M rows and 15 columns.
<br>
The first 3 rows of the dataset is shown below:

|      | CBSA Code | Date | AQI |Category| Defining Param |Number of Sites Reporting | city_ascii | state_id | state_name | lat | lng | population | density | timezone |
|-----:|-----------|------|-----|--------|---------|---------------------------|------------|----------|------------|-----|-----|------------|---------|----------|
|     0| 10140 |2022-01-01| 21 | Good | PM2.5 | 2 | Aberdeen | WA | Washington | 46.9757 | -123.8094 | 16571.0 | 588.0 | America/Los_Angeles |
|     1| 10140 |2022-01-02| 12 | Good | PM2.5 | 2 | Aberdeen | WA | Washington | 46.9757 | -123.8094 | 16571.0 | 588.0 | America/Los_Angeles |
|     2| 10140 |2022-01-03| 18 | Good | PM2.5 | 2 | Aberdeen | WA | Washington | 46.9757 | -123.8094 | 16571.0 | 588.0 | America/Los_Angeles |


### Data Wrangling and Analysis
We converted the Date column to a datetime object, and cleaned up some of the timezone values. More information can be found in the Jupyter notebook and the report.

<br>
Exploratory data analysis concludes the following: 
* The west coast, especially California, is more prone to extreme AQI values.
* The cleanest cities seem to have small populations and are not from California.
