# Vacation
Load Data
* Use pandas to load the city weather CSV into a dataframe

Create map visualization
* Use hvplot to create a dynamic map plotting city locations
* Size markers based on humidity value for each city

Filter ideal weather conditions
* Use pandas filtering to narrow down to cities meeting ideal weather criteria
* Criteria like max temperature range, wind speeds etc.

Find nearest hotels
* Create new dataframe to store hotel info for cities
* Use Geoapify Places API to find closest hotel within 10km of coordinates
* Store hotel name back into dataframe

Plot map with hotel info
* Create map visualization with filtered city/hotel data
* Size based on humidity, tooltip shows hotel details

So in summary, the key libraries used are Pandas, HVPlot, and the Requests library to query the Geoapify API and plot hotel/weather data on interactive maps.

# Weather

Generate Random Geographic Coordinates
* Uses NumPy's `random.uniform()` method to generate 1500 random latitudes and longitudes. 
* Combines them into `lat_lngs` list of coordinate tuples.

Identify Nearest Cities
* Uses `citipy` module to identify the nearest city for each latitude/longitude combination.
* Adds unique city names to a `cities` list.

Fetch Weather Data 
* Uses OpenWeatherMap API to retrieve weather data for each city.
* Makes API requests in batches of 50 cities to stay within rate limits.
* Parses JSON response to extract relevant weather data like temperature, humidity, etc.
* Appends each city's weather data to `city_data` list.

Save to DataFrame
* Converts `city_data` to a Pandas DataFrame for easier analysis.
* Exports DataFrame to a CSV file.

Key Library Imports
The main libraries used include:

* Matplotlib, Pandas, Numpy, Requests, Citipy, Datetime
* API Keys loaded from external file

Scatter Plot DataFrame
Create Scatter plots to capture key DataFrame info and compute linear regression for each of the following: 
* Latitude Vs. Temperature
* Latitude Vs. Humidity
* Latitude Vs. Cloudiness
* Latitude Vs. Wind Speed Plot