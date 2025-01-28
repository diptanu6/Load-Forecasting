# Electricity Load Forecasting Project

## Project Overview
This project involves forecasting electricity load consumption for a specific date (December 14, 2020) based on historical load demand and weather data. The project uses a Random Forest Regressor to predict the load and includes steps for data preprocessing, feature engineering, and handling missing data.

## Features
- **Historical Load Data Analysis**: Analyze and visualize historical electricity load data.
- **Data Preprocessing**: Handle missing data using interpolation and feature engineering.
- **Load Prediction**: Train a Random Forest Regressor model to predict the electricity load.
- **Validation**: Evaluate the model’s performance using the Mean Absolute Percentage Error (MAPE).
- **Forecasting**: Generate a load forecast for a date not present in the dataset (December 14, 2020).

## Prerequisites
To run the project, you need the following libraries installed:

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## File Structure
- **assignment-data.csv**: Input dataset containing historical load and weather data.
- **task1_forecast_dec14_load.csv**: Output file containing the forecasted load for December 14, 2020.
- **task2_filled.csv**: Output file with missing load values filled.
- **main_script.py**: Main script for load forecasting.
- **README.md**: This file, describing the project.

## Data Preprocessing
1. **Datetime Conversion**:
   - Convert the `datetime` column to a datetime type and set it as the index.
2. **Missing Data Handling**:
   - Use time-based interpolation to fill missing weather-related data.
3. **Feature Engineering**:
   - Generate additional features like:
     - `hour`: Hour of the day
     - `day_of_week`: Day of the week
     - `is_weekend`: Boolean indicating whether it is a weekend
     - `month`: Month of the year
     - `is_holiday`: Boolean indicating whether the day is a holiday

## Steps to Run the Code
1. Clone or download the project repository.
2. Place the dataset (`assignment-data.csv`) in the project directory.
3. Run the main script (`main_script.py`).
   ```bash
   python main_script.py
   ```
4. The script will:
   - Train the model using data up to December 13, 2020.
   - Predict the electricity load for December 14, 2020.
   - Save the results in `task1_forecast_dec14_load.csv`.
   - Fill missing load values in the dataset and save the updated dataset in `task2_filled.csv`.

## Outputs
1. **Forecast for December 14, 2020**:
   - The predicted load for December 14, 2020, is saved in `task1_forecast_dec14_load.csv`.
2. **Filled Dataset**:
   - A dataset with missing load values filled is saved in `task2_filled.csv`.

## Code Explanation
### Model Training
- A `RandomForestRegressor` is used for predicting the load.
- The model is trained using data up to December 13, 2020.
- A validation set is created using a train-test split, and MAPE is calculated to evaluate model performance.

### Forecasting for December 14, 2020
- Features for December 14, 2020, are manually created based on its characteristics (e.g., day of the week, holiday status).
- The trained model is used to predict the load for this date.

### Filling Missing Values
- Missing load values in the dataset are filled using predictions from the trained model.

## Example Output
**Predicted load for December 14, 2020**:
```
Predicted load for 2020-12-14: 150.25 MW
```
The output is also saved in `task1_forecast_dec14_load.csv`.

## Limitations
- The accuracy of the forecast depends on the quality and completeness of the historical data.
- Holidays and other special events might need additional manual handling for accurate predictions.

## Contact
For any questions or issues, feel free to contact:
**Diptanu Biswas**
- Email: officialdiptanu01@gmail.com

---
Thank you for using this project!

