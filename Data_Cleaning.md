# Data Cleaning procedure

## Dealing with nan values

* Dropped rows with missing information on target variable (actual_delivery_time) 
* Filled missing values in market_id and order_protocol from likelihood based on the store_id
* Used 'other' for missing values in store_primary_category
* Used KNNImputer(n=50) to fill missing values for the columns regarding number of dashers available using the day of the week and hour of the day and the region of the store(market_id).
* Dropped the remaining rows with missing values
* Dropped store_id

## Category Encoding

* Used one-hot encoding for market_id, store_primary_category, order_protocol, and day of the week
* Used ordinal encoding for hour of the day

## Feature Engineering

* Removed time-stamp columns and introduced hour of the day and day of the week and the target variable - actual_delivery_time(seconds)

## Files

* Data_Cleaning.ipynb - Jupyter notebook with the code for data cleaning
* historical_data.csv - Initial dataset
* filled_data.csv - Dataset after taking care of missing values
* categorical_data.csv - Dataset after encoding categorical variables
* df_clean.csv - Final dataset after data cleaning