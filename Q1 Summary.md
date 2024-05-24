# Q3 Summary Report
## Data Import and Cleaning:
Data from timeseries_data.xlsx was loaded and cleaned, with missing values addressed using forward filling to maintain the continuity of the time series data.
## Exploratory Data Analysis:
Key variables were visualized over time to understand their distribution and interactions.
Correlations among RTLMP, wind generation, solar generation, and actual load were analyzed, revealing moderate correlations that inform the impact of generation types on pricing.
## Feature Engineering:
Comprehensive feature engineering was undertaken to enhance the predictive capabilities of the modeling:
Time-related features such as hour of the day, day of the week, and month were added.
Lagged features for RTLMP, wind, and solar generation were created up to 24 hours to capture temporal dependencies.
Rolling window statistics (mean and standard deviation) for key variables over 24-hour periods were calculated.
## Model Choice:
Similar to the stock prediction task done in my ML course, an LSTM (Long Short-Term Memory) model was chosen for its proficiency in handling sequence prediction problems, ideal for time series data like RTLMP.
## Data Preparation for LSTM:
Data was normalized using Min-Max scaling.
The dataset was reshaped to fit the LSTM input requirements and split into training and validation sets.
## Model Training and Evaluation:
The initial LSTM model setup included layers with dropout to prevent overfitting.
The model was trained, and performance metrics (MAE and RMSE) were planned for evaluation.
## Conclusion and Improvement:
The LSTM model shows promise for accurately forecasting RTLMP based on the prepared features. Adjustments and optimizations in model architecture and hyperparameters are recommended to enhance model performance.
Further exploration into hybrid models combining LSTM with other neural network architectures could provide improvements in capturing both temporal and spatial dependencies.
Experimenting with additional features and alternative modeling techniques such as ensemble methods or hybrid deep learning models could yield better predictive accuracy.
