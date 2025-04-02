# RSI_314 short readme
python code for LSTM model that uses RSI (Relative Strength Index) function financial data integrated from PostgreSQL. This tool is not intended for use as a standalone source of data but rather as tool in concert with data indicators to provide a more holistic view. this tool was developed using multiple forms of AGI to be used to teach python and understand the syntax and how that works with regards to training a LTSM (neural network). Any questions or comments are greatly appreciated. Feel free to share or mod etc.

#RSI_314 the whole enchilada con salsa (RSI Prediction using LSTM)

## Description
This project implements a financial analysis tool that predicts the Relative Strength Index (RSI) of selected stock tickers using Long Short-Term Memory (LSTM) neural networks. The tool fetches historical stock data, computes the RSI, and trains an LSTM model to predict future RSI values.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Contributing](#contributing)
- [Contact](#contact)

## Installation
To set up the project, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/wifiknight45/RSI_314/blob/main/F_Multi_Stock_RSI_Predictor_ready2run

    Install the required packages:
    Make sure you have Python 3 installed. You can create a virtual environment and install the dependencies using pip:

bash

pip install numpy pandas yfinance matplotlib scikit-learn tensorflow

Run the script:
Execute the script to start processing the stock tickers:

bash

    python rsi_prediction.py

Usage

The script processes a predefined list of stock tickers, computes their RSI, and predicts future RSI values. The results are saved in CSV files and visualized using Matplotlib.
Parameters

    tickers: List of stock tickers to analyze (default: ['AAPL', 'MSFT', 'WF', 'SBUX', 'TASK']).
    start_date: Start date for fetching historical data (default: '2020-01-01').
    end_date: End date for fetching historical data (default: '2024-01-01').
    rsi_window: Window size for RSI calculation (default: 14).
    sequence_length: Length of sequences for LSTM input (default: 50).
    epochs: Number of training epochs for the LSTM model (default: 25).
    batch_size: Batch size for training (default: 32).

Output

The script generates:

    CSV files containing actual and predicted RSI values for each ticker in the rsi_predictions directory.
    Plots comparing actual and predicted RSI values.

License

This project is licensed under the MIT License. See the LICENSE file for details.
Contributing

Contributions are welcome! If you would like to contribute to this project, please follow these steps:

    Fork the repository.
    Create a new branch (git checkout -b feature/YourFeature).
    Make your changes and commit them (git commit -m 'Add some feature').
    Push to the branch (git push origin feature/YourFeature).
    Create a new Pull Request.

Contact

For questions or support, please contact:

    Your Name - vichy6@proton.me
    GitHub: @wifiknight45

