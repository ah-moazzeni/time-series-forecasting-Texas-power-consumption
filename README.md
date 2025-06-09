# Time Series Forecasting: Texas ERCOT Power Consumption

## Project Overview

This project focuses on building and comparing various time series forecasting models to predict daily power consumption in Texas, specifically data from the Electric Reliability Council of Texas (ERCOT). The goal is to evaluate the performance of different modeling approaches, ranging from traditional statistical models to deep learning recurrent neural networks, in accurately forecasting future power demand.

## Data

The analysis is based on historical daily power consumption data from ERCOT.

The dataset covers approximately 6 years of daily power consumption.

## Methodology

The project explores the following forecasting models:

1.  **Long Short-Term Memory (LSTM) Network:** A type of Recurrent Neural Network (RNN) well-suited for sequence prediction, capable of learning long-term dependencies.
2.  **Simple Recurrent Neural Network (SimpleRNN):** A foundational RNN model, simpler than LSTM, used to establish a baseline for deep learning approaches.
3.  **Bidirectional LSTM (BiLSTM) Network:** An extension of LSTM that processes sequence data in both forward and backward directions to capture richer context.
4.  **Facebook Prophet:** A robust forecasting library designed for business time series with strong seasonal effects and holidays.

Each model is trained on a rigorously defined training set, validated on a separate validation set, and finally evaluated on a held-out test set to ensure realistic performance assessment. Data scaling and sequence generation are applied as appropriate for the neural network models.

## Key Findings

Interestingly, in this analysis, the **SimpleRNN model demonstrated competitive (and in some metrics, superior) performance** compared to the more complex LSTM and BiLSTM architectures, and significantly outperformed Facebook Prophet on the test set.

| Model        | MSE          | RMSE        | MAE        | MAPE (%) |
| :----------- | :----------- | :---------- | :--------- | :------- |
| **LSTM** | 4296583.32   | 2072.82     | 1563.84    | 2.99     |
| **SimpleRNN**| **4122326.28** | **2030.35** | **1518.15**| **2.94** |
| **BiLSTM** | 4513408.13   | 2124.48     | 1620.54    | 3.13     |
| **Prophet** | 22775838.63  | 4772.40     | 3628.61    | 7.08     |

