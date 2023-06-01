


# Forecasting Mid-Price Movement with Machine Learning Methods

This repository contains code for forecasting mid-price movement in the financial market using machine learning methods. The code utilizes XGBoost, CatBoost, and LSTM classifiers to predict whether the mid-price of a financial commodity (ICICI Bank or Aluminium) will increase, remain the same, or decrease over a 5-day period.

## Prerequisites

- Python 3.x
- Required Python packages can be installed by running:

  ```bash
  pip install -r requirements.txt
  ```

## Getting Started

1. Clone the repository:

   ```bash
   git clone <repository_url>
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Data Preprocessing:
   - Place your input data file(s) in the appropriate directory.
   - Run the preprocessing script to preprocess the data and perform feature engineering:

     ```bash
     python preprocessing.py
     ```

4. Trimming Data:
   - Run the trimming script to filter the data within the specified time range:

     ```bash
     python trim.py
     ```

5. XGBoost Classifier Pipeline:
   - Run the XGBoost classifier pipeline script to train models, evaluate their performance, and generate accuracy matrices:

     ```bash
     python xgboost_classifier.py
     ```

6. CatBoost Classifier Pipeline:
   - Run the CatBoost classifier pipeline script to train models, evaluate their performance, and generate accuracy matrices:

     ```bash
     python catboost_classifier.py
     ```

7. LSTM Classifier Pipeline:
   - Run the LSTM classifier pipeline script to train models, evaluate their performance, and generate accuracy matrices:

     ```bash
     python lstm_classifier.py
     ```

8. Results:
   - Classification reports for each parameter are saved in the respective `report` directories.
   - Accuracy matrices for each parameter are saved in the respective `accuracy_matrices` directories.
   - Prediction results are saved in the `prediction.csv` file.

## Project Structure

- `preprocessing.py`: Preprocesses the input data file(s) and performs feature engineering.
- `trim.py`: Filters the data within the specified time range.
- `xgboost_classifier.py`: Trains XGBoost classifiers, evaluates their performance, and saves the results.
- `catboost_classifier.py`: Trains CatBoost classifiers, evaluates their performance, and saves the results.
- `lstm_classifier.py`: Trains LSTM classifiers, evaluates their performance, and saves the results.
- `data/`: Directory to store input data file(s).
- `final_new_data/results/XGB Classifier/`: Directory to store XGBoost classifier results.
- `final_new_data/results/Catboost Classifier/`: Directory to store CatBoost classifier results.
- `final_new_data/results/LSTM Classifier/`: Directory to store LSTM classifier results.
- `final_new_data/results/XGB Classifier/report/`: Directory to store XGBoost classifier classification reports.
- `final_new_data/results/Catboost Classifier/report/`: Directory to store CatBoost classifier classification reports.
- `final_new_data/results/LSTM Classifier/report/`: Directory to store LSTM classifier classification reports.
- `final_new_data/results/XGB Classifier/accuracy matrices/`: Directory to store XGBoost classifier accuracy matrices.
- `final_new_data/results/Catboost Classifier/accuracy matrices/`: Directory to store CatBoost classifier accuracy matrices.
- `final_new_data/results/LSTM Classifier/accuracy matrices/`: Directory to store LSTM classifier accuracy matrices.
- `prediction.csv`: File to store prediction results.

## Contributing

Contributions to this project are welcome
