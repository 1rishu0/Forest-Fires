# Algerian Forest Fire Prediction
This project predicts forest fire occurrences in Algeria using meteorological and environmental data, as well as Fire Weather Index (FWI) components. The dataset contains observations from June to September 2012. The project leverages Ridge and Lasso regression models to predict fire risks based on weather conditions and provides a web-based interface using Flask, HTML, and CSS.

## Dataset Description
The dataset contains the following columns:

**Day:** Day of the observation (DD).
**Month:** Month of the observation (June to September).
**Year:** Year of the observation (2012).
**Temperature (Temp):** Temperature at noon in Celsius degrees (22 to 42).
**Relative Humidity (RH):** Relative humidity in % (21 to 90).
**Wind Speed (Ws):** Wind speed in km/h (6 to 29).
**Rain:** Total daily rainfall in mm (0 to 16.8).

## FWI Components
The dataset includes Fire Weather Index (FWI) system components, which help assess fire risks based on weather and fuel conditions.

- **Fine Fuel Moisture Code (FFMC):** Measures surface litter moisture content (28.6 to 92.5).
- **Duff Moisture Code (DMC):** Measures moisture content in the duff layer (1.1 to 65.9).
- **Drought Code (DC):** Indicates long-term drought conditions (7 to 220.4).
- **Initial Spread Index (ISI):** Measures potential fire spread rate (0 to 18.5).
- **Buildup Index (BUI):** Combines DMC and DC to indicate fire intensity potential (1.1 to 68).
- **Fire Weather Index (FWI):** General fire intensity index (0 to 31.1).
- **Classes:** Binary target variable indicating fire occurrence (Fire or Not Fire).

## Regions
The dataset covers two regions within Algeria, allowing for region-based analysis of fire risks.

# Project Workflow

## 1. Data Preprocessing
- **Data Cleaning:** Handle missing values and outliers.
- **Feature Scaling:** Normalize data for consistent input to the machine learning models.
- **Feature Selection:** Use Lasso regression to identify the most influential features in predicting forest fires.

## 2. Model Training
- **Ridge Regression:** Helps handle multicollinearity among features, improving model stability and accuracy.
- **Lasso Regression:** Performs feature selection by penalizing less significant variables, improving model interpretability.
- **Evaluation Metrics:** Evaluate model performance using metrics such as Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared.

## 3. Web Application
The project includes a web application built with Flask, HTML, and CSS to make the prediction tool accessible.

- **User Input:** Users can input temperature, humidity, wind speed, rain, and FWI component values to receive fire risk predictions.
- **Visualization:** The app displays predicted fire risk in a user-friendly format.

## How to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/1rishu0/Forest-Fires
   cd Forest-Fires

2. **Install Requirements**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Flask App**:
    ```bash
    flask run
    ```

4. **Access the Web Application**:  
   Open `http://127.0.0.1:5000` in your web browser to use the application.

## Conclusion

This project combines machine learning and web technologies to provide an accessible tool for predicting forest fires in Algeria. By analyzing weather and FWI components, the model offers valuable insights into fire risks, aiding in early detection and prevention strategies to protect Algeria's forests and communities.
