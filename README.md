# Harnessing Weather Insights for Accurate Energy Load Forecasting

by Florian Schulze, Raffaela Länger, Johanna Kronfuß and Julian Janisch

------------

## Goal of this project

This project focuses on developing a short-term load forecasting model for predicting Austria’s energy consumption by combining two distinct datasets: weather data from GeoSphere Austria (2021) and historical energy consumption data from ENTSO-E (n.d.). Since weather conditions significantly impact electricity demand, affecting heating, cooling, and overall energy usage, we analyze the relationship between these variables and energy consumption using machine learning techniques.

## Data Used

To make meaningful predictions about Austria’s energy consumption, we used two primary datasets:
- **Weather Data**: Collected from GeoSphere Austria, this dataset includes various meteorological parameters such as temperature, wind speed, cloud cover, air pressure, and sunshine duration. These factors influence energy demand by affecting heating and cooling needs.
- **Energy Consumption Data**: Sourced from the ENTSO-E Transparency Platform, this dataset provides historical electricity usage in Austria. It is used as the target variable in our forecasting models.

Both datasets were accessed via API, allowing automated retrieval and streamlined pre-processing. Additionally, we performed data cleaning and feature engineering to enhance model accuracy.

## Project Workflow

To execute this project, the following steps must be followed:

1. **Run the `download_data.ipynb` notebook** to automatically retrieve weather and energy consumption data via API. This step ensures structured and error-free data collection.
2. **Preprocess and clean the data** to align the datasets, remove inconsistencies, and format the information for further analysis.
3. **Execute the `regression_model.ipynb` notebook** to train different models, including Linear Regression and Random Forest, and evaluate their performance.
4. **Perform feature engineering**, where additional features are generated to improve the model’s predictive accuracy, including cyclic transformations for time-based variables.
5. **Evaluate and compare models** using key metrics such as Root Mean Squared Error (RMSE) and R² to select the best-performing approach.

## Results and Performance

The best-performing model was the Random Forest Regressor, which achieved:

- RMSE: **381.14 MW**
- R²: **0.92**

While the model successfully predicted regular energy consumption patterns, it faced difficulties on special days with significant variations in demand. This issue likely arose due to the limited number of such days in the training dataset.

## Societal and Business Relevance

Energy load forecasting is crucial for balancing supply and demand, optimizing energy distribution, and integrating renewable sources for a more sustainable grid. Given the geopolitical uncertainties following Russia’s exit from European energy markets, precise energy consumption forecasting is vital for ensuring stability and efficiency in Austria’s power sector.

## Challenges and Solutions

- **Data Licensing**: The datasets used are available under the Creative Commons Attribution 4.0 license, enabling their integration and public sharing.
- **Model Accuracy**: Feature engineering, such as cyclic encoding of time-related data, significantly improved model performance.
- **Transparency & Reproducibility**: Detailed documentation and structured workflow ensure that the project remains transparent and easy to replicate.

## Future Enhancements

Future iterations of this project could integrate additional influencing factors such as socioeconomic variables, electricity prices, and industrial activity to improve predictions. More advanced machine learning models, such as neural networks and gradient boosting, could be explored to enhance accuracy. Expanding the model to predict regional energy consumption within Austria would provide more localized insights, and adapting the approach for international energy consumption forecasting could make it applicable to other countries. These enhancements would further refine the model and increase its real-world usability.

## License

This project is released under the **Creative Commons Zero v1.0 Universal (CC0 1.0) License**, making it freely available for use and modification.

---

*This project utilizes publicly available data from GeoSphere Austria and ENTSO-E, both licensed under Creative Commons Attribution 4.0.*

