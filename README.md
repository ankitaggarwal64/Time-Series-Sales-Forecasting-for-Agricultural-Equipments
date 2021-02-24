# Time Series Forecasting for Agricultural Equipments


### Table of Contents

1. [Project Overview](#Overview)
2. [Problem Statement](#Statement)
3. [Files Description](#files)
4. [Dependencies](#Dependencies)
5. [Results Summary](#Summary)
6. [Future Scope](#Scope)

## Project Overview<a name="Overview"></a>
In today’s world, the success of the organization is dependent on how much they can reduce and control the uncertainty in their system. The first and most important step in reducing the uncertainty is to better predict the sales of their products.
In this project, we would like to develop sales forecasting models for predicting the monthly sales of an agricultural equipment .Along with the available past monthly sales data, we will also consider other relevant data including economic and commodity indices which might be helpful for our forecasting.

For reading about the insights generated with this project please read this[blog post on Medium.](https://ankitaggarwal64.medium.com/how-time-series-forecasting-can-predict-sales-546ed030767a)

## Problem Statement<a name="Statement"></a>
Our goal for the project is to develop monthly sales forecasting model which can accurately predict sales for two months ahead in future i.e forecast horizon of two months. We selected two months period as the forecast horizon as for automobile manufacturers most of decisions regarding supply chain(including components ordering for manufacturing the final product) are confirmed two months in advance of the target sales month.

## Files Description <a name="files"></a>

The files structure is arranged as below:

	- README.md: read me file
	- Project Overview and Data Ingestion.ipynb: provides oveview of project and ingest data
	- Data_Understanding(EDA).ipynb: exploratory data analysis and data prepration
	- Feature_selection.ipynb: implementation of Boruta method for features selection
	- Univariate_ARIMA.ipynb: implmentation of ARIMA for forecasting
	- Multivariate_Regression_with_ARIMA.ipynb: implementation of SARIMAX for forecasting and results comparison
	- results_summary : snapshot of model results comparison summary

## Dependencies <a name="Dependencies"></a>

- Python 3.*
- Statmodels
- Boruta, Sklearn
- Matplotlib, Seaborn, pylab
- NumPy, Pandas

## Results Summary<a name="Summary"></a>
Based on model comparison between univaraite ARIMA and multivariate SARIMAX as shown in below table, we can clearly see that ARIMA model performs better in all metrics. This means that either the predictive information that we tried to include in our forecasting model was not relevant or our model was not able to learn the relationship between sales and precdictive variables.
![alt text](https://github.com/ankitaggarwal64/Time-Series-Sales-Forecasting-for-Agricultural-Equipments/blob/main/results_summary.JPG)
  
## Future Scope<a name="Scope"></a>
- Until now we have experimented with ARIMA based Statistical models which are linear models and will not be able to learn non-linear paterns. Experimenting further with machine learning and deep learning models like LSTM which have ability to learn complex patterns can help in improving the performance.
- There are also other well known methods such as Prophet method which can also be experimented to look for improvement posibilities.


