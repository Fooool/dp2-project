# Harnessing Weather Insights for Accurate Energy Load Forecasting

by Florian Schulze, Raffaela Länger, Johanna Kronfuß and Julian Janisch

------------

## Goal of this project
This project aims to predict energy consumption in Austria by integrating energy consumption data from the ENTSO-E Transparency Platform and real-time weather data from GeoSphere Austria. By combining these data sources, we seek to analyze the correlation between weather conditions and energy consumption patterns, ultimately improving energy demand forecasting for the next 48 hours.

## Short explanation of the methods
To achieve this, we utilize linear regression for predicting energy consumption and apply K-Means clustering to analyze weather patterns. The data processing pipeline is powered by Apache Spark to handle large datasets efficiently, while Matplotlib is used for visualization purposes.

## Data sources used
The energy consumption data is sourced from the ENTSO-E Transparency Platform and accessed via SFTP or REST API. Weather data is obtained from GeoSphere Austria through their FTP server and requires extensive filtering to ensure accuracy. To validate our approach, we compare our predictions with official energy forecasts to assess the reliability of our models.
