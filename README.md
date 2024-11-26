# Time Series Analysis and PM2.5 Forecasting using LSTM in Hyderabad

## Project Overview

This project employs time series analysis and an LSTM recurrent neural network to analyze and predict PM2.5 levels in Hyderabad, India. The dataset spans from July 1, 2017, to June 30, 2024, encompassing daily measurements of various air pollutants, including PM2.5, PM10, wind speed (WS), wind direction (WD), temperature (Temp), and relative humidity (RH). The project focuses on data preprocessing, handling missing values, exploratory data analysis (EDA), and building an LSTM model to forecast PM2.5 concentrations.

## Motivation

Air pollution, particularly PM2.5, poses a significant threat to public health in urban areas like Hyderabad. Accurate forecasting of PM2.5 levels can contribute to:

* **Public Health Awareness:**  Informing citizens about potential high-pollution days, enabling them to take precautionary measures.
* **Policy Decisions:** Supporting policymakers in implementing targeted interventions to mitigate pollution levels.
* **Early Warning Systems:** Developing systems that alert authorities and the public about impending high-pollution events.


## Dataset Overview

The dataset comprises daily measurements of air pollutants in Delhi, covering the period from July 1, 2017, to June 30, 2024.

* **Link:** [Central Pollution Control Board (CPCB)](https://cpcb.nic.in/)

**Features:**

* **Timestamp (Index):** Date of the measurement (YYYY-MM-DD).
* **PM2.5:** Concentration of Particulate Matter 2.5 (µg/m³).
* **PM10:** Concentration of Particulate Matter 10 (µg/m³).
* **WS:** Wind Speed (m/s).
* **WD:** Wind Direction (degrees).
* **Temp:** Temperature (°C).
* **RH:** Relative Humidity (%).

## Instructions to Run

This project uses a Jupyter Notebook (.ipynb) for analysis. It is recommended to run it in a Google Colab environment due to the computational requirements of LSTM models.

**1. Running in Google Colab:**

* Open the notebook in Colab: [Insert Colab link here]
* Connect to a runtime (GPU recommended)
* Run the cells sequentially.

**2. Running Locally:**

* **Prerequisites:** Python 3.7+
* **Clone the repository:** `git clone [Your GitHub Repository URL]`
* **Navigate to the project directory:** `cd [Your Project Directory]`
* **Create and activate a virtual environment (recommended):**
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate  # On Linux/macOS
    .venv\Scripts\activate  # On Windows
    ```
* **Install dependencies:** `pip install -r requirements.txt`
* **Start Jupyter:** `jupyter notebook`
* **Open and run the notebook:** Open the .ipynb file.


## Dependencies

See `requirements.txt`.


## Methodology

1. **Data Loading and Preprocessing:** Loading the CSV data, handling missing values using mean imputation, and converting the timestamp to a DateTimeIndex.
2. **Exploratory Data Analysis (EDA):** Creating time series plots for each pollutant, generating descriptive statistics, visualizing feature distributions and potential outliers using histograms and box plots, and performing correlation analysis using a heatmap. Additionally, a monthly average analysis of PM2.5 levels is conducted.
3. **Normalization and Preprocessing:** Filling remaining missing values with the mean, normalizing the data using MinMaxScaler, and creating sequences of data for LSTM input.
4. **LSTM Model Building:** Defining the architecture of the LSTM model, including LSTM layers, dropout for regularization, and dense layers.
5. **Model Training:** Training the LSTM model using the Adam optimizer and mean squared error (MSE) loss, incorporating early stopping to prevent overfitting.  Validation data used during training.
6. **Model Evaluation:** Evaluating model performance using RMSE, MAE, MAPE, and R-squared metrics, and visualizing actual vs. predicted PM2.5 values using an overlay chart.

## Conclusion

While the LSTM model shows promise for PM2.5 prediction, this project serves as a starting point for further research. Future work could involve incorporating external data sources (e.g., meteorological information, traffic patterns), exploring alternative deep learning architectures, and optimizing hyperparameters for improved accuracy. Real-time data integration and deployment as a predictive service could also be considered.
## Author & Contact 

* **GitHub:** [ratulbanik](https://github.com/ratulbanik)
* **LinkedIn:** [https://www.linkedin.com/in/ratul-banik/](https://www.linkedin.com/in/ratul-banik/)  