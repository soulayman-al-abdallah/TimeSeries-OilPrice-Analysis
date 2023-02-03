# TimeSeries-OilPrice-Analysis
Oil Price Time series data analysis and modeling using ARIMA, Prophet and LSTM.

- [Running the app](https://github.com/soulayman-al-abdallah/TimeSeries-OilPrice-Analysis#running-the-app)
- [Dataset](https://github.com/soulayman-al-abdallah/TimeSeries-OilPrice-Analysis#dataset)
- [Model Training](https://github.com/soulayman-al-abdallah/TimeSeries-OilPrice-Analysis#training)
- [ARIMA](https://github.com/soulayman-al-abdallah/TimeSeries-OilPrice-Analysis#arima)
- [PROPHET](https://github.com/soulayman-al-abdallah/TimeSeries-OilPrice-Analysis#prophet)
- [LSTM](https://github.com/soulayman-al-abdallah/TimeSeries-OilPrice-Analysis#lstm)
- [Contact information](https://github.com/soulayman-al-abdallah/TimeSeries-OilPrice-Analysis#contact-information)




## Running the app

You can run the app by clicking on the colab notebooks, while replacing the "github" domain with "githubtocolab", if it takes long time to load. 



-----
## Dataset

Used Data of oil prices from [here](https://github.com/soulayman-al-abdallah/public-repo.git)

7641 rows × 2 columns
From 1987-05-20	to 2017-06-26


<img width="945" height="300" alt="Screenshot 2023-02-03 at 6 02 42 PM" src="https://user-images.githubusercontent.com/75330691/216656711-a042ad33-b985-474b-b079-2c22e6a57f4f.png">


## Training

I trained multiple models as  we can see:

- 1- **ARIMA**: The model stands for AutoRegressive Integrated Moving Average.

- 2- **PROPHET**: Prophet by Facebook as an algorithm for the in-house prediction of time series values

- 3- **LSTM**: Long short term memory deep neural network model


## **ARIMA**: 

**Additive Data Decomposition** is used to extract the Trend, Seasonality and Residual components from a dataset containing oil prices.

<img width="945" height="300" alt="Screenshot 2023-02-03 at 6 03 22 PM" src="https://user-images.githubusercontent.com/75330691/216660737-c34a2094-b5a4-4220-b063-e1458b5461b9.png">


**Stationarity check** through:
- Visual Interpretation of rolling mean and rolling std
- Summary statistics
- Standard statistics (ADF and KPss)

If data is not stationary, we can use either **Difference transform** or **Logarithmic transform:**

<img  width="945" height="300" alt="Screenshot 2023-02-03 at 6 04 31 PM" src="https://user-images.githubusercontent.com/75330691/216661620-7b28c578-a056-4283-9919-3ac389872807.png">


**ARIMA** model stands for AutoRegressive Integrated Moving Average. The model has 3 hyperparameters -

  - p: The AutoRegressive model's parameter. It defines the no. of past obsevations that help determine the current observation.

  - d: The order of differencing. It defines the order to which differencing operation needs to be carried out in order to make the data stationary. In our data we have already converted the data to a stationary form, so ideally this parameter should be 1.

  - q: The Moving Average model's parameter. This is used to define the no. of white noise terms(of previous observations) that help to describe the current observation.

<img width="300" alt="Screenshot 2023-02-03 at 6 06 47 PM" src="https://user-images.githubusercontent.com/75330691/216661875-a5425153-cc84-4630-a3fc-7e84efccd3f7.png">



## **PROPHET**: 

Prophet by Facebook as an algorithm for the in-house prediction of time series values.

Additive model of multiple components:

yt = g(t) + s(t) + h(t) + εt

- g(t): represents the trend, to capture the general trend of the series
- s(t): represents the seasonality, to model the seasonal trend (seasonal ads)
- h(t): represents the cycle (holidays)
- εt: represents the error term

<img width="598"  height="300" alt="Screenshot 2023-02-03 at 6 09 11 PM" src="https://user-images.githubusercontent.com/75330691/216662170-8948f0d0-91d9-4fcc-8c9c-f5d5a8206b38.png">


## **LSTM**: 

Long short term memory deep neural network model

Data split percentage: 80% for training and 20% for testing

<img width="458" height="300" alt="Screenshot 2023-02-03 at 7 02 22 PM" src="https://user-images.githubusercontent.com/75330691/216663266-5a84a390-002d-457f-a706-a1907c2b49ce.png">

Predictions vs True values:

<img width="1173" height="300" alt="Screenshot 2023-02-03 at 6 10 40 PM" src="https://user-images.githubusercontent.com/75330691/216663350-9f8a589d-365f-445a-b18f-1468373faeab.png">





## Contact information

For any further information about this repository's work, do not hesitate to reach me through LinkedIn:

[Eng. Soulayman Al-Abdallah](http://linkedin.com/in/soulayman-al-abdallah)
