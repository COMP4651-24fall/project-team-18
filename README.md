[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/jzfQvm5J)

# Comp4651_Project

This repo is for Fall2024 Comp4651 final project.

## Description of each source file

- `data-processing.ipynb`: This notebook is used to implement feature engineering and add new features including the 10-day Simple Moving Average (SMA-240), 20-day Simple Moving Average (SMA-480), 14-day Relative Strength Index (RSI) and Bollinger Bands with a period of 20 days which consist of the Middle Band, the Upper Band, the Lower Band and the standard deviation (STD).
- `linear-regression.ipynb`: This notebook is used to train and evaluate the linear regression model on the preprocessed data. It contains result of the model evaluation such as RMSE and R-Squared and other information related to the model.
- `random-forest.ipynb`: This notebook is used to train and evaluate the random forest model on the preprocessed data. It contains result of the model evaluation such as RMSE and R-Squared and other information related to the model.
- `back-test.ipynb`: This notebook is used to carry out the back testing on the subset of Bitcoin market data from January, 2023 to October, 2024. This will apply 4 different trading strategies with two being traditional trading strategies and the remaining two using the prediction from Linear Regression and Random Forest model respectively to make investment decisions. Metrics such as total profit/loss, Win/Loss ratio, etc will be used to test the strategies' performance.

## Reference

Modified From https://github.com/aws-solutions-library-samples/guidance-for-digital-assets-on-aws/tree/main:

- `load-marketdata.ipynb`: This notebook is used to download the dataset and upload them to a s3 bucket

## Suggested Running Order

1. Run `load-marketdata.ipynb` to load the data and upload to the s3 bucket (need to change to your bucket name in the file)
2. Run `data-processing.ipynb` to preprocess the data
3. Run `linear-regression.ipynb` and `random-forest.ipynb` to analyze the dataset and test the capacity of Spark
4. Run `back-test.ipynb` to verify the effectiveness of the model and gain more insight

## Running Environment

The notebooks are running on the AWS SageMaker Studio JupyterLab environment. The space settings of JupyterLab are with instance of ml.t3.medium. image of SageMaker Distribution 2.1.0 and storage of 5GB. Lastly, glueSpark will be used as the notebooks’ kernel.
