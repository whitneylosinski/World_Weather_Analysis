# World Weather Analysis

## Purpose

A coworker at PlanMyTrip requested help in collecting and analyzing weather data across over 500 cities worldwide to be used for recommending ideal hotels to their customers based on the clients' weather preferences.  Specifically, the coworker requested that the Google Maps and Places API and Search Nearby features be used to create a heat map that displays the following information about each city:

1. A Hotel in the City
2. City Name
3. Country Code
4. Current Weather Condition 
5. Maximum Temperature

## Resources

 - Data source: schools_complete.csv & students_complete.csv
 - Software: Python 3.8, Anaconda Navigator (anaconda3), Jupyter Notebook (anaconda3)

## Results:

This analysis was completed in three major steps which are described below.

1. ) **Collecting the Data:**  
The first step of the project was to collect the data.  To do this, the Numpy module was used to generate 2000 random latitude and longitudes as shown in the following code.
    ```py
    # Create a set of random latitude and longitude combinations.
    lats = np.random.uniform(low = -90.000, high=90.000, size=2000)
    lngs = np.random.uniform(low=-180.000, high=180.000, size=2000)
    lat_lngs = zip(lats, lngs)
    lat_lngs
    ```
    
 - Use the NumPy module to generate more than 1,500 random latitudes and longitudes.
 - Use the citipy module to list the nearest city to the latitudes and longitudes.
 - Use the OpenWeatherMap API to request the current weather data from each unique city in your list.
 - Parse the JSON data from the API request.
 - Collect the following data from the JSON file and add it to a DataFrame:
 - City, country, and date
 - Latitude and longitude
 - Maximum temperature
 - Humidity
 - Cloudiness
 - Wind speed
2. ) Exploratory Analysis with Visualization:
Create scatter plots of the weather data for the following comparisons:
 - Latitude versus temperature
 - Latitude versus humidity
 - Latitude versus cloudiness
 - Latitude versus wind speed
Determine the correlations for the following weather data:
 - Latitude and temperature
 - Latitude and humidity
 - Latitude and cloudiness
 - Latitude and wind speed
Create a series of heatmaps using the Google Maps and Places API that showcases the following:
 - Latitude and temperature
 - Latitude and humidity
 - Latitude and cloudiness
 - Latitude and wind speed
3. ) Visualize Travel Data:
Create a heatmap with pop-up markers that can display information on specific cities based on a customer's travel preferences. Complete these steps:
 - Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.
 - Create a heatmap for the new DataFrame.
 - Find a hotel from the cities' coordinates using Google's Maps and Places API, and Search Nearby feature.
 - Store the name of the first hotel in the DataFrame.
 - Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city.
 
 ## Summary
