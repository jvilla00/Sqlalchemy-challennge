# Sqlalchemy-challennge
---------------------------------------------------
For this Repo I perform a precipitation analysis and then a station analysis.

#### Precipitation Analysis

* Found a recent date in the dataset.
* Using the date, retrieved the previous 12 months of precipitation data by querying the 12 previous months of data. 
* Selected only the `date` and `prcp` values.
* Loaded the query results into a Pandas DataFrame, and set the index to the date column.
* Sorted the DataFrame values by `date`.
* Ploted the results by using the DataFrame `plot` method
* Used Pandas to print the summary statistics for the precipitation data.

#### Station Analysis

* Designed a query to calculate the total number of stations in the dataset.
* Designed a query to find the most active stations (the stations with the most rows).
    * Listed the stations and observation counts in descending order.
    * Chose the station id that had the highest number of observations.
    * Used the most active station id, and calculate the lowest, highest, and average temperatures.

* Designed a query to retrieve the previous 12 months of temperature observation data (TOBS).
    * Filtered by the station with the highest number of observations.
    * Queried the previous 12 months of temperature observation data for this station.
    * Ploted the results as a histogram with `bins=12`.
    
- - -
### Part 2: Designed a Climate App

Used Flask to create routes
* `/`
    * Homepage.
    * Lists all available routes.

* `/api/v1.0/precipitation`
    * Converted the query results to a dictionary using `date` as the key and `prcp` as the value.
    * Returned the JSON representation of to a dictionary.

* `/api/v1.0/stations`
    * Returned a JSON list of stations from the dataset.

* `/api/v1.0/tobs`
    * Queried the dates and temperature observations of the most active station for the previous year of data.
    * Returned a JSON list of temperature observations (TOBS) for the previous year.

* `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`
    * Returned a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a given start or start-end range.

