# Real-Time Flood Prediction and Alert System

This project is a machine learning-based system designed to predict the risk of floods using real-time weather data. It includes a web dashboard built with Flask for user interaction, map visualization, and an SMS alert system using Twilio.

## Features
- **Real-Time Prediction:** Enter a city name to fetch current weather data (temperature, humidity, wind speed, rainfall) from the OpenWeather API.
- **Machine Learning Model:** Uses a pre-trained XGBoost model to predict flood risk ("High" or "Low") based on the weather data.
- **Interactive Dashboard:** A web interface built with Flask to input data and display results.
- **Map Visualization:** Integrates with Leaflet.js to show the location of the queried city on a map.
- **SMS Alerts:** If a high flood risk is detected, the system automatically sends a warning SMS to a predefined list of users via the Twilio API.

## Technologies Used
- **Backend:** Python, Flask
- **Machine Learning:** Scikit-learn, XGBoost, LightGBM, Pandas, NumPy
- **APIs & Services:** OpenWeather API, Twilio, ngrok
- **Frontend:** HTML, CSS, JavaScript, Leaflet.js
- **Environment:** Google Colab / Jupyter Notebook

## Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git)
    cd YOUR_REPOSITORY_NAME
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Create an environment file:**
    Create a file named `.env` in the root directory and add your API keys:
    ```
    TWILIO_SID=YOUR_TWILIO_ACCOUNT_SID
    TWILIO_AUTH_TOKEN=YOUR_TWILIO_AUTH_TOKEN
    TWILIO_PHONE=YOUR_TWILIO_PHONE_NUMBER
    # Note: The OpenWeather API key is currently hardcoded in app.py.
    # For better security, it should also be moved to this .env file.
    ```

## Usage
1.  Run the Flask application:
    ```bash
    python app.py
    ```
2.  The application will start, and ngrok will provide a public URL. Open this URL in your browser.
3.  Enter a city name in the input field and click "Predict".
4.  The dashboard will display the current weather, flood risk, and SMS alert status.
