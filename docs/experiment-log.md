# Machine Learning Experiment Log

This document records the experiments, results, observations and lessons learned throughout the Nepal 24K Gold Price Forecasting project.

## Experiment 01 — Decision Tree Regressor

**Objective:** Establish an initial machine learning model for predicting gold prices.

**Results:**
- MAE: NPR 91,137.51
- RMSE: NPR 112,962.36
- R²: -1.865

**Observation:** The model struggled to predict prices in the testing period, particularly because prices increased substantially compared with the training period.

**Conclusion:** Decision Trees struggled to generalise to the higher price range.

## Experiment 02 — Random Forest Regressor

**Objective:** Test whether an ensemble of decision trees could improve prediction accuracy.

**Results:**
- MAE: NPR 91,080.25
- RMSE: NPR 112,857.52
- R²: -1.8597

**Observation:** Random Forest performed marginally better than the Decision Tree, but prediction errors remained very high.

**Conclusion:** Combining decision trees did not solve the underlying forecasting problem.

## Experiment 03 — Linear Regression

**Objective:** Test a simpler statistical model using the three previous gold prices as input features.

**Results:**
- MAE: NPR 1,706.64
- RMSE: NPR 3,049.65
- R²: 0.9979

**Observation:** Linear Regression performed significantly better than the tree-based models.

**Conclusion:** A simple linear relationship between previous and current prices captured much of the short-term price movement.

## Experiment 04 — ARIMA

**Objective:** Explore a traditional time-series forecasting approach.

**Configuration:** ARIMA(1, 1, 1)

**Results:**
- MAE: NPR 90,670.70
- RMSE: NPR 112,582.43
- R²: -1.8457

**Observation:** The model performed poorly on the testing period.

**Conclusion:** This particular ARIMA configuration did not capture the price behaviour effectively.

## Experiment 05 — Feedforward Neural Network

**Objective:** Explore whether a basic neural network could learn patterns from previous gold prices.

**Architecture:**
- Input: 3 features
- Hidden layer: 8 neurons
- Activation: ReLU
- Output: 1 neuron

**Training configuration:**
- Optimizer: Adam
- Loss function: Mean Absolute Error
- Epochs: 50
- Batch size: 32

**Results:**
- MAE: NPR 2,795.76
- RMSE: NPR 4,609.64
- R²: 0.9952

**Observation:** The neural network achieved a high R² score but performed worse than both the baseline and Linear Regression.

**Conclusion:** A more complex model does not necessarily produce better predictions.

## Overall Observations

The experiments so far suggest that:
1. Simple models can outperform more complex algorithms.
2. The substantial increase in gold prices during the testing period presents a challenge for several models.
3. Model evaluation should consider multiple metrics rather than relying only on R².
4. A baseline model is essential for determining whether machine learning actually adds predictive value.

## Next Steps

- Experiment with LSTM neural networks.
- Explore additional features.
- Investigate ways to improve forecasting performance.
- Continue comparing models against the baseline.

*This log will be updated as the project progresses.*
