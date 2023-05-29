A Machine Learning pipeline for forecasting the mid-price movement of two financial commodities (ICICI Bank and Aluminium) using various features extracted from the data. Let's break down the code and provide an explanation for each step along with some relevant theory.

    Data Preprocessing:
    The code starts by reading the data from the given file path using pandas' read_csv function. It then performs some preprocessing steps on the data. However, the code provided only includes a partial snippet, so it's difficult to provide a complete understanding of the preprocessing steps being performed.

    Feature Engineering:
    After preprocessing, the code proceeds with feature engineering. It creates additional features based on the existing data, such as bid-ask spreads, mid-prices, price differences, mean prices, volumes, accumulated differences, price and volume derivatives, average intensity indicators, relative intensity indicators, and accelerations (market/limit).

Feature engineering aims to create informative and relevant features that can improve the performance of machine learning models. It involves transforming raw data into a representation that captures meaningful patterns and relationships.

    Label Generation:
    Next, the code generates labels for each data entry row based on the mid-price using two different statistical formulas. The labels are assigned values of -1, 0, or 1, indicating whether the mid-price in the future will decrease, remain the same, or increase, respectively. This step involves comparing the values obtained from the statistical formulas to a threshold value (alpha) to determine the label.

    Model Training and Evaluation:
    The code then proceeds to train and evaluate machine learning models for forecasting mid-price movement. It uses three different models: XGBoost, CatBoost, and LSTM.

    XGBoost: XGBoost is an optimized gradient boosting framework that provides efficient implementations of gradient boosting algorithms. The code uses XGBClassifier from the XGBoost library for classification.

    CatBoost: CatBoost is another gradient boosting library that provides state-of-the-art performance. The code uses CatBoostClassifier from the CatBoost library for classification.

    LSTM: Long Short-Term Memory (LSTM) is a type of recurrent neural network (RNN) architecture that is well-suited for sequential data analysis. However, the code snippet provided does not include the implementation of LSTM.

The code splits the data into train and test sets based on the date, performs model training using the train set, and evaluates the model's performance on the test set. The evaluation metrics used include accuracy, F1 score, precision, and other accuracy metrics. The classification reports are saved in separate text files.

    Results and Output:
    The code generates accuracy matrices for each model and saves them as CSV files. Additionally, it saves the predicted labels (Yt_pred) in a separate CSV file called "prediction.csv".



```
# Forecasting Mid-Price Movement with Machine Learning Methods

This repository contains code for forecasting mid-price movement in the financial market using machine learning methods. The code utilizes XGBoost, CatBoost, and LSTM classifiers to predict whether the mid-price of a financial commodity (ICICI Bank or Aluminium) will increase, remain the same, or decrease over a 5-day period.

## Prerequisites

- Python 3.x
- Required Python packages can be installed by running:
  ```
  pip install -r requirements.txt
  ```

## Getting Started

1. Clone the repository:
   ```
   git clone <repository_url>
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Data Preprocessing:
   - Place your input data file(s) in the appropriate directory.
   - Run the preprocessing script to preprocess the data and perform feature engineering:
     ```
     python preprocessing.py
     ```

4. Trimming Data:
   - Run the trimming script to filter the data within the specified time range:
     ```
     python trim.py
     ```

5. XGBoost Classifier Pipeline:
   - Run the XGBoost classifier pipeline script to train models, evaluate their performance, and generate accuracy matrices:
     ```
     python xgboost_classifier.py
     ```

6. CatBoost Classifier Pipeline:
   - Run the CatBoost classifier pipeline script to train models, evaluate their performance, and generate accuracy matrices:
     ```
     python catboost_classifier.py
     ```

7. LSTM Classifier Pipeline:
   - Run the LSTM classifier pipeline script to train models, evaluate their performance, and generate accuracy matrices:
     ```
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

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please submit a pull request
