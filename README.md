# Weather Data Analysis and Visualization Project

## Project Overview
This project involves collecting, analyzing, and visualizing weather data from over 500 cities around the globe to understand the relationship between weather variables and latitude. The project is divided into two main parts:

  1. Weather Analysis (WeatherPy.ipynb): Utilizing the OpenWeatherMap API to retrieve weather data and create scatter plots to showcase relationships between latitude and various weather parameters.

  2. Vacation Planning (VacationPy.ipynb): Using the Geoapify API and GeoViews to map ideal vacation spots based on preferred weather conditions and nearby hotels.


## Table of Contents
  Project Overview
  Prerequisites
  Installation
  Data Sources
  Files Description
  Usage
  Part 1: Weather Analysis (WeatherPy.ipynb)
  Part 2: Vacation Planning (VacationPy.ipynb)
  Results
  Conclusion

## Prerequisites
Before you begin, ensure you have met the following requirements:
  - Python 3.x installed on your machine.
  - Jupyter Notebook or JupyterLab installed.
  - API keys for:
    -OpenWeatherMap API
    -Geoapify API

## Installation
1. Clone the Repository:
  git clone https://github.com/yourusername/WeatherDataAnalysis.git
2. Navigate to the Project Directory:
3. Install Required Packages:
  - pandas
  - numpy
  - matplotlib
  - requests
  - scipy
  - hvplot
  - geoviews
  - holoviews
  - cartopy
  - citipy
4. Set Up API Keys:
  - Create a file named api_keys.py in the project directory.
  - Add your API keys to the file:
    weather_api_key = "YOUR_OPENWEATHERMAP_API_KEY"
    geoapify_key = "YOUR_GEOAPIFY_API_KEY"

## Data Sources
OpenWeatherMap API: Provides current weather data for cities worldwide.
Geoapify Places API: Used to find nearby hotels for given coordinates.

## Files Description
- WeatherPy.ipynb: Jupyter Notebook for weather data analysis.
- VacationPy.ipynb: Jupyter Notebook for mapping ideal vacation spots.
- output_data/: Directory containing output CSV files and figures.
- api_keys.py: Python script containing API keys (not included in the repository for security reasons).

## Usage
### Part 1: Weather Analysis (WeatherPy.ipynb)
1. Generate City List:
  - Randomly generate a list of over 500 cities using the citipy library based on random latitude and longitude combinations.
2. Fetch Weather Data:
  - Use the OpenWeatherMap API to retrieve weather data for each city.
  - Handle any errors or missing data appropriately.
3. Create Scatter Plots:
  - Latitude vs. Temperature
  - Latitude vs. Humidity
  - Latitude vs. Cloudiness
  - Latitude vs. Wind Speed
4. Perform Linear Regression:
  - Separate data into Northern and Southern Hemispheres.
  - Compute linear regression for each relationship.
  - Plot regression lines and calculate the r-squared values.
5. Observations:
  - Provide analysis and insights based on the visualizations and regression results.

### Part 2: Vacation Planning (VacationPy.ipynb)
1. Filter Ideal Cities:
  - Narrow down cities based on ideal weather conditions (e.g., temperature range, humidity, cloudiness).
2. Find Nearest Hotels:
  - Use the Geoapify API to find the nearest hotel within 10,000 meters of each city's coordinates.
  - Add hotel names to the DataFrame.
3. Create a Map with Hotels:
  - Use GeoViews and hvPlot to create a world map.
  - Plot the cities with markers, where each marker size represents humidity.
  - Include hover information displaying city name, country, and hotel name.

## Results

### Part 1: Weather Analysis
- Temperature: There's a clear correlation between latitude and temperature. Temperatures increase as you move closer to the equator (latitude 0°).
- Humidity, Cloudiness, Wind Speed: These variables show weaker correlations with latitude, suggesting they are influenced by other factors.
### Part 2: Vacation Planning
- Ideal Cities: A list of cities matching the ideal weather conditions was generated.
- Hotel Mapping: The nearest hotels to these cities were identified and plotted on an interactive map for visualization.


## Conclusion
This project demonstrates how to leverage public APIs and data visualization libraries to analyze and present weather data. The insights gained can be valuable for various applications, including vacation planning, climate studies, and educational purposes.
