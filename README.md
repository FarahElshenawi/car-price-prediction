# Car Price Prediction Project
![Car Price Prediction](img/webapp.png) 

This project is an end-to-end machine learning pipeline for predicting car prices based on various vehicle features. It leverages a dataset containing information about car manufacturers, models, fuel types, and other characteristics to build a predictive model using Python. The project incorporates data preprocessing, exploratory data analysis (EDA), feature engineering, and model training. A Streamlit web application is also developed to provide a user-friendly interface for predicting car prices based on user inputs.
## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Modeling](#modeling)
- [Evaluation Metrics](#evaluation-metrics)
- [Web Application](#web-application)
- [Usage](#usage)




## Introduction

The aim of this project is to predict the prices of used cars based on various factors such as the car's manufacturer, model, year of production, mileage, engine size, and more. The final prediction is powered by a machine learning model that has been trained on historical car sales data.

## Dataset

The dataset used in this project includes car listings with multiple features:
- Manufacturer (e.g., Lexus, Chevrolet, Honda)
- Model (e.g., RX 350, Accord, Volt)
- Fuel Type (e.g., Gasoline, Diesel)
- Mileage
- Engine Volume
- Year
- Transmission (e.g., Automatic, Manual)
- Drive Type (e.g., AWD, FWD)
- Color, and more.

The dataset is publicly available and included in the repository as `car_price_prediction.csv`.

 ## Project Structure

```plaintext
car-price-prediction/
│
├── data/                         
│   └── car_price_prediction.csv    # The dataset used for training
├── app.py                          # Streamlit app for deployment
├── model/
    └──  car_prediction.sav         # Trained machine learning model
├── README.md                       # Project documentation          
└── notebook/
    └── Car_Price.ipynb
```
## Modeling

### Data Preprocessing

The preprocessing steps include:
- **Handling missing values**: Ensuring that all missing data points are addressed to avoid any bias in predictions.
- **Encoding categorical features**: This includes encoding features such as manufacturer, model, fuel type, and others into numerical formats suitable for the model.
- **Normalizing numerical features**: Normalization is applied to features like mileage and engine volume to bring them onto a similar scale, improving the model's performance.
- **Feature engineering**: This step involves creating new features that can enhance the model's predictive capabilities, such as converting the year of the car to its age.

### Model

The model is trained using the **Random Forest Regressor**, a powerful and interpretable machine learning algorithm for regression tasks. The model predicts car prices based on the cleaned and encoded features, leveraging multiple decision trees to improve accuracy and control overfitting.

## Evaluation Metrics

The performance of the model is evaluated using the following metrics:
- **Root Mean Squared Error (RMSE)**: This metric measures the average magnitude of the errors in a set of predictions, with a higher penalty for larger errors.
- **R-squared (R²) Score**: This statistic provides an indication of how well the independent variables explain the variability of the dependent variable (car prices in this case).

## Web Application

A web application has been built using **Streamlit** to allow users to input car features and get price predictions. The app features a user-friendly interface where users can select car attributes and view the predicted price instantly.

## Usage

### Running the Streamlit App

To run the app locally:
1. Ensure that all the dependencies are installed. You can install them using
2. Run the following command in your terminal
    ```bash
    streamlit run app.py
    ```
Once the app is running, it will open in your browser, allowing you to input car details and receive an estimated price prediction.
### Sample Input and Prediction

1. **Select the Manufacturer** (e.g., Honda).
2. **Select the Model** (e.g., Civic).
3. **Provide additional details** such as Mileage, Fuel Type, Transmission, Year, etc.
4. **Click the Predict button** to get the predicted price.

## Results

The machine learning model has been evaluated on a test dataset, and it provides reasonably accurate predictions. The Random Forest model achieved the following performance on the test set:

- **Root Mean Square Error (RMSE)**:  5168.932288
- **R-squared Score**:  0.798337

   
