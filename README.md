# Forecasting COVID-19 Vaccination Progress in South Asia

## Project Overview
This project focuses on forecasting the progress of COVID-19 vaccination in Bangladesh, India, and Pakistan over the next 180 days using advanced time series models. By employing Hidden Markov Model (HMM), Autoregressive Integrated Moving Average (ARIMA), and Seasonal ARIMA (SARIMA), the study aims to provide accurate predictions to support policymakers and healthcare authorities in resource allocation and targeted interventions to accelerate immunization efforts and mitigate the spread of the virus.

## Objectives
- Predict daily vaccination progress in Bangladesh, India, and Pakistan.
- Compare the performance of HMM, ARIMA, and SARIMA models using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).
- Provide actionable insights for public health decision-making.

## Dataset
The dataset used in this study contains time series data on COVID-19 vaccination progress in Bangladesh, India, and Pakistan. https://www.kaggle.com/datasets/gpreda/covid-world-vaccination-progress

## Methodology
The project implements a robust time series forecasting pipeline:
- **Data Preprocessing**: Conducted by A K M Nihalul Kabir, including cleaning and structuring the dataset for time series analysis.
- **Model Selection**: Three models were applied:
  - **Hidden Markov Model (HMM)**: Captures hidden states in vaccination trends.
  - **ARIMA**: Models non-seasonal time series patterns.
  - **SARIMA**: Accounts for seasonal trends in vaccination data.
- **Evaluation Metrics**: Models were assessed using MAE, MSE, and RMSE to measure prediction accuracy.
- **Forecasting**: Predictions were generated for the next 180 days of vaccination progress in each country.

## Results
- **Bangladesh**: ARIMA outperformed SARIMA and HMM, achieving the lowest MAE (17,143.82), MSE (8.217e+09), and RMSE (769.95).
- **India**: ARIMA showed superior performance with an MAE of 21,617.68, MSE of 1.56 billion, and RMSE of 95,122, while SARIMA performed slightly better in some metrics (MSE: 857 million, RMSE: 29,271.37). HMM had significantly higher errors (MAE: ~1.65 billion, MSE: ~2.95e+18).
- **Pakistan**: SARIMA demonstrated the best performance, with the lowest MAE (11,487.483), MSE (2.19e+14), and RMSE, outperforming ARIMA and HMM.
- **Overall**: SARIMA exhibited the most consistent performance across all regions, particularly in Pakistan, while ARIMA excelled in Bangladesh and India. HMM consistently showed the highest errors.

## Repository Contents
- `code/`: Python scripts for data preprocessing, model implementation, and evaluation.
- `notebooks/`: Jupyter notebooks for exploratory data analysis and model comparisons.
- `report/`: Project report (`Forecasting the vaccination progress of COVID-19 ML.pdf`) detailing methodology, results, and conclusions.
- `visualizations/`: Figures comparing model performance and forecasting results for each country.

## Getting Started
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   Required libraries include `pandas`, `numpy`, `statsmodels`, and `hmmlearn`.
3. **Run the Code**:
   - Execute the main script or Jupyter notebooks to preprocess data, train models, and generate forecasts.
   - Ensure the dataset is available in the `data/` directory (refer to the project report for source details).

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
