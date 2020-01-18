# tableau-citibike-analysis
December 15, 2019

## OVERVIEW ##
* [Tableau Public - Analysis of Citi Bike NYC Trip Data 2018](https://public.tableau.com/profile/jlcatx512#!/vizhome/NYC_Citi_Bike_Trip_Data_2018_Analysis/2018NYCCitiBike)
* I analyzed 2018 data because it was the most recent year with all 12 months.
* The original data can be download [here](https://www.citibikenyc.com/system-data).
* I cleaned and pre-processed the data in Google Colab because cleaning data in Tableau is a total pain in the ass.
* The cleaning and pre-processing steps taken included:
    * Dropping all rows with null values.
    * Dropping any rider claiming to be over 80 years old.
    * Dropping any short trips, which might indicate an aborted ride, i.e. < 10 minutes and the start and end stations are the same.
* I'm not including the actual processed csv file on Github because it was enormous. About 3 GB. But if you take all the 2018 csv files, combine and then run them through the Jupyter notebook code, you will get the same file. 

## Observation 1 - Demographic patterns ##
1. Rider age slopes up to 30 years old and then steadily declines. But there is a strange outlier: a large spike in riders claiming to be 49 years old. I didn't normalize this because I felt like there might be an unexplained reason for this.
2. Subscribers far outnumber one-off customers, which suggests the popularity of the Citi Bike program.
3. Men far outnumber women. Encouraging more women to ride would be a big opportunity for growth.

## Observation 2 - Seasonal and time of day patterns ##
* There is a clear seasonal pattern to bike use. Rides peak in the summer and decrease in the winter. e.g. June has roughly 3x  January riders.
* In both summer and winter, there is a clear dual-peak commuting pattern to ride usage. Ride counts peaks at 8 AM and 5 PM, which roughly corresponds to business hours.

## Observation 3 - Geographic ##
* Pershing Square North is by far the most popular place to start and end a ride. This makes intuitive sense since it is next to Grand Central Station, which is Manhattan's main transportation hub.

## ACTION ITEMS ##
- [X] change username.
- [X] http://www.devops-blog.net/tips-and-tricks/unzip-multiple-files-in-same-directory-on-mac-os-x

## LINKS ##
* [Assignment](https://github.com/the-Coding-Boot-Camp-at-UT/UT-MCB-DATA-PT-07-2019-U-C/tree/e6683622422df8106f72aeeaa8c8b058b59fc5b6/homework-instructions/20-Tableau/Instructions)
* https://www.citibikenyc.com/
* https://www.citibikenyc.com/system-data
* https://s3.amazonaws.com/tripdata/index.html

## TIPS ##
* Use GCP BigDataQuery
* TIP:
> just to give you a hint, New York city bike data is also available on GCP BigQuery as a free public data set. The ETL is done for you. You can pull BigQuery tables directly to Tableau (not sure about the free version).
> 
> oh, bigquery result can be saved to a federated table, which means you can save it to google drive or google sheet