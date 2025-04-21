# RSI_314
python code for LSTM model that uses RSI (Relative Strength Index) function financial data integrated from PostgreSQL. This tool is not intended for use as a standalone source of data but rather as tool in concert with data indicators to provide a more holistic view. this tool was developed using multiple forms of AGI to be used to teach python and understand the syntax and how that works with regards to training a LTSM (neural network). Any questions or comments are greatly appreciated. Feel free to share or mod etc. 

# Multi-Stock RSI Predictor using LSTM

This project predicts the Relative Strength Index (RSI) for multiple stocks using a Long Short-Term Memory (LSTM) neural network. It downloads stock data, computes the RSI, trains an LSTM model on the computed RSI, and makes predictions. The results are saved as CSV files and plotted for visual analysis.

---

## Features

1. **Stock Data Download**: Automatically fetches stock price data for the specified tickers using Yahoo Finance.
2. **RSI Calculation**: Computes the RSI for each stock based on the closing prices.
3. **LSTM Model**: Trains an LSTM model to predict RSI values.
4. **Visualization**: Plots actual RSI versus predicted RSI for visual comparison.
5. **Batch Processing**: Processes multiple stock tickers sequentially.
6. **Output Storage**: Saves predictions to CSV files for further analysis.

---

## Installation and Requirements

### Required Libraries
Install the following Python libraries before running the script:
- `numpy`
- `pandas`
- `yfinance`
- `matplotlib`
- `scikit-learn`
- `tensorflow`

You can install them using pip:
```bash
pip install numpy pandas yfinance matplotlib scikit-learn tensorflow
```

---

## Parameters

- **Tickers**: List of stock symbols to process (e.g., `['AAPL', 'MSFT', 'WF', 'SBUX', 'TASK']`).
- **Start Date**: Start date for historical stock data (e.g., `'2020-01-01'`).
- **End Date**: End date for historical stock data (e.g., `'2025-03-14'`).
- **RSI Window**: Window size for RSI calculation (default: `14`).
- **Sequence Length**: Number of time steps used for LSTM training (default: `50`).
- **Epochs**: Number of epochs to train the LSTM model (default: `25`).
- **Batch Size**: Batch size for LSTM training (default: `32`).

---

## How It Works

1. **Input Validation**:
   - Validates stock ticker symbols to ensure they contain only alphanumeric characters.

2. **RSI Calculation**:
   - Computes RSI based on stock closing prices using a specified window size.

3. **Data Preparation**:
   - Scales RSI values to the range `[0, 1]` using MinMaxScaler.
   - Creates sequences of RSI values for training and testing the LSTM model.

4. **LSTM Model**:
   - Builds a sequential LSTM model with 50 units and a Dense output layer.
   - Trains the model using Mean Squared Error (MSE) loss and the Adam optimizer.

5. **Prediction and Visualization**:
   - Predicts RSI values for the test dataset.
   - Saves predictions to CSV files (`rsi_predictions/{ticker}_rsi_predictions.csv`).
   - Plots actual RSI versus predicted RSI.

---

## File Structure

- **Code File**: Script to execute the entire pipeline.
- **Output Directory**: `rsi_predictions/` (created automatically) contains CSV files with the results.

---

## Usage

1. Clone the repository:
```bash
git clone https://github.com/wifiknight45/RSI_314.git
cd RSI_314
```

2. Run the script:
```bash
python F_Multi_Stock_RSI_Predictor_ready2run.py
```

3. View predictions:
   - CSV files are saved in the `rsi_predictions/` directory.
   - Plots are displayed for each stock showing actual vs predicted RSI.

---

## Example Output

**Prediction CSV**:
```
Date,Actual_RSI,Predicted_RSI
2025-03-10,65.23,64.98
2025-03-11,63.45,63.89
...
```

**Sample Plot**:
- Green Line: Actual RSI
- Red Line: Predicted RSI
- Orange Line: Overbought threshold (70)
- Purple Line: Oversold threshold (30)

---

## Error Handling

- Invalid ticker symbols are skipped with an appropriate error message.
- Any unexpected errors during processing are logged, and the script continues with the next ticker.

---

## Notes

- The LSTM model is trained and evaluated independently for each stock ticker.
- Ensure that the `start_date` and `end_date` cover a sufficient range to compute meaningful RSI values.

---

## License

This project is licensed under the [MIT License](LICENSE).
