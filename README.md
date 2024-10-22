# Analysis-of-Air-Quality-and-Electric-Vehicle-Registrations-in-Bengaluru

## Overview
This project analyzes the relationship between electric vehicle (EV) registrations and air quality in Bengaluru using real-world data. The analysis explores air pollutant trends over time, the impact of EV registrations, and emissions by fuel type. Various visualization techniques and statistical models, such as linear regression, are used to interpret the data.

## Dataset
The analysis uses an Excel dataset with multiple sheets:
- **Bengaluru AQI**: Contains air quality data, including various pollutants (PM2.5, PM10, NOx, CO2, etc.), indexed by date.
- **Fuel type Registration Vehicle**: Contains the number of vehicle registrations by fuel type, including electric vehicles, indexed by month.
- **Vehicle Emission Dataset**: Contains vehicle emissions data, including CO2, NOx, and PM2.5 emissions, based on vehicle attributes like fuel type, engine size, etc.

## Requirements
To run the code, ensure you have the following libraries installed:
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `numpy`

Install these using the following command:
```bash
pip install pandas matplotlib seaborn scikit-learn numpy
```

## Files
- `MS Main Dataset.xlsx`: The main dataset containing air quality, vehicle registration, and emission data across three sheets.

## Code Breakdown

### 1. Data Loading and Preprocessing
The data is loaded from an Excel file using `pandas`:
- Air quality data from the "Bengaluru AQI" sheet.
- Vehicle registration data from the "Fuel type Registration Vehicle" sheet.
- Emission data from the "Vehicle Emission Dataset" sheet.

All datasets are cleaned by dropping rows with missing values and ensuring the date formats are correct.

### 2. Pollutant Trend Analysis
We analyze the time series trends for pollutants such as PM2.5, PM10, NOx, CO2, SO2, and O3 in Bengaluru using line plots. This visualizes changes in pollution levels over time.

### 3. EV Registration Trends
Summing EV registrations by month, the code creates a time series plot showing how EV registrations have evolved over time.

### 4. Vehicle Emission Analysis by Fuel Type
The code calculates the average emissions (CO2, NOx, and PM2.5) based on fuel type and visualizes the results using bar plots. Each pollutant is plotted separately, with annotations for easy interpretation.

### 5. Correlation Matrix
A correlation heatmap is generated to analyze relationships between vehicle attributes (such as engine size, age, and mileage) and emissions (CO2, NOx, PM2.5). This helps understand how various factors are interconnected.

### 6. Linear Regression Analysis
The final analysis performs a linear regression to examine the relationship between EV registrations and air quality (AQI). The model is trained on a portion of the data, and predictions are evaluated on a test set using Mean Squared Error and R-squared values.

A scatter plot is generated to compare actual and predicted AQI values based on EV registrations.

### Interpretation
- **Pollutant Trends**: Over time, pollutants show variations, with certain pollutants showing reductions or increases depending on factors such as seasonality or policy interventions.
- **EV Registrations**: The growth in EV registrations suggests an increasing adoption of cleaner technologies, possibly impacting pollution levels.
- **Emissions by Fuel Type**: The average emissions per fuel type highlight the environmental impact of different vehicle types, with electric vehicles expected to have lower emissions compared to internal combustion engines.
- **Regression Model**: The linear regression analysis shows a relationship between EV registrations and AQI, though the strength of the model will depend on the `R-squared` value.

## Results
- **Mean Squared Error**: The error between predicted and actual AQI values.
- **R-squared**: The proportion of variance explained by the model.

## Visualization
The code generates multiple plots, including:
1. **Time Series Plots**: For each pollutant in Bengaluru.
2. **EV Registration Trends**: Time series for EV registration growth.
3. **Bar Plots**: Average emissions by fuel type.
4. **Correlation Heatmap**: For vehicle attributes and emissions.
5. **Scatter Plot**: Actual vs predicted AQI values.

## Running the Code
To run the code:
1. Ensure the dataset `MS Main Dataset.xlsx` is placed in the working directory.
2. Run the Python script to load and preprocess the data, generate visualizations, and run the regression model.

## Conclusion
This project demonstrates the use of Python for analyzing air quality data, vehicle registrations, and emissions. It provides insights into the potential impact of EV adoption on air quality and contributes to discussions on sustainable transportation.

---

### License
This project is licensed under the MIT License. See the LICENSE file for details.

### Author
Suhas G R

### Acknowledgments
Special thanks to the data sources and open-source libraries used in this project.
