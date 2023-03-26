# datathon
### problem statement
In the financial industry, credit charge offs are a crucial metric to measure as they directly impact the health of the institution. A charge off occurs when a customer fails to make payment and eventually is written off as a loss. With that, it is increasingly important for banks to accurately forecast their charge offs in order to make informed decisions for the future.

Based on customer and macroeconomic data, forecast an accurate number of monthly charge offs over the period of February 2020 thru January 2021.

### dataset
we are given training dataset, test dataset(forecast_starting_data.csv) and macro dataset which contains US economic context dataset. The training dataset is not uploaded to the github because of the file size.

### preprocess
Each dataset is preprocessed accordingly with preprocess - python files. The python files create training_for_account_ver.csv, training_for_aggregated_ver.csv, test_for_account_ver.csv, and test_for_aggregated_ver.csv. Each dataset is training or test dataset for 2 different models(account ver and aggregated ver).

### model
The machine learning models used to predict the result is in the ml_model_account_ver.ipynb and ml_model_aggregated_ver.ipynb file. The account ver models are binary classification models, predicting the chargeoff flag of each customer account. The aggregated ver models are regression models, predicting the ratio of monthly chargeoff customers.

### accuracy
The aggregated ver models showed better accuracy than the account ver models. We used autoML for the aggregated ver models. Random Forest Regressor, Gradient Boosting Regressor, Extreme Gradient Boosting and AdaBoost Regressor showed 0.004 RMSE in training dataset.

### final result
The final prediction result is saved in the results_RAINING.csv file.