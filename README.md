# Time Series Forecasting with LSTM on Air Passengers Dataset

This project demonstrates how to forecast the monthly number of air passengers using Long Short-Term Memory (LSTM) networks in Python.

## Dataset

The dataset used in this project is the classic "Air Passengers" dataset, which contains monthly totals of international airline passengers from 1949 to 1960.

## Libraries Used

- NumPy
- Pandas
- Matplotlib
- Scikit-learn (for MinMaxScaler)
- Keras (for LSTM, Dense, Dropout layers and model building)

## Steps

1. **Data Loading and Preprocessing:**
   - Load the dataset using Pandas.
   - Convert the 'Month' column to datetime objects and set it as the index.
   - Normalize the data using MinMaxScaler.
   - Split the data into training and testing sets (80% for training, 20% for testing).

2. **Data Preparation for LSTM:**
   - Create a function to prepare the data for LSTM input, where previous time steps are used to predict the next step.
   - Reshape the data into a 3D format: (samples, time steps, features).

3. **Building and Training the Model:**
   - Create an LSTM model using Keras with two LSTM layers, dropout layers for regularization, and a Dense output layer.
   - Compile the model using the Adam optimizer and mean squared error loss function.
   - Train the model on the training data.

4. **Model Predictions and Rescaling:**
   - Make predictions on both the training and testing data.
   - Inverse transform the predictions to get the actual passenger numbers.

5. **Plotting Predictions against Actual Data:**
   - Plot the actual passenger numbers, training predictions, and testing predictions on a single graph.

6. **Model Evaluation with RMSE:**
   - Calculate the Root Mean Squared Error (RMSE) to evaluate the model's performance on both training and testing sets.


## How to Run

1. **Install necessary libraries:**
