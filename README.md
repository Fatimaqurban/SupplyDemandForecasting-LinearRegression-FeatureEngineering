**Supply-Demand Forecasting for Ride-Hailing Services**

**Background:**
The project focuses on supply-demand forecasting for ride-hailing services, particularly for Uber, in City M during the year 2016. With over 11 million trips processed daily, accurate forecasting is essential for maximizing driver utilization and ensuring rider satisfaction. The aim is to predict the supply-demand gap for specific regions and time slots, facilitating efficient allocation of resources.

**Definition:**
Supply-demand forecasting involves predicting the number of passengers' requests and drivers' answers (supply) for each region and time slot. This enables Uber to anticipate demand surges and guide drivers accordingly, leading to higher earnings for drivers and better service for riders. The task requires applying regression algorithms to predict the supply-demand gap based on historical data.

**Data Format:**
- Training set: Contains three consecutive weeks of data for City M in 2016.
- Test set: Contains data for the fourth and fifth weeks of City M. Each test instance includes half an hour before the predicted time slot.
- Order Information Table: Contains basic information about orders, including order ID, driver ID, passenger ID, origin, destination, price, and timestamp.
- Region Information Table: Provides information about regions, including region hash and region ID.

**Code Overview:**
1. Load and preprocess order data, including merging with the cluster map to obtain region IDs and converting timestamps to time slots.
2. Calculate demand (total orders), supply (fulfilled orders), and the gap (demand-supply) for each region and time slot.
3. **Feature Engineering:** Derive new features or transform existing ones to enhance model performance and capture relevant information.
4. Train regression models (Linear Regression, kNN Regression, Decision Tree Regression) to predict the supply-demand gap.
5. Evaluate model performance using metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared.
6. Provide predictions for specific test instances.
7. Visualize actual vs. predicted values for model comparison.

**Readme:**
To use this code:
1. Ensure Python and necessary libraries (NumPy, pandas, scikit-learn, matplotlib, seaborn) are installed.
2. Download the order data and cluster map from the provided paths.
3. Run the code in a Python environment, adjusting file paths if necessary.
4. Review model performance metrics and visualizations to assess forecasting accuracy.
5. Use trained models for predicting the supply-demand gap in real-time scenarios.
