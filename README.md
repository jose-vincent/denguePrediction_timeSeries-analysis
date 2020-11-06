# Dengue Prediction using Time Series Analysis

* **_Predict the expected number of Dengue fever cases to start a contingency plan to confront the Dengue spread._**

* **_ARIMA, SARIMA & prophet models are used for Time series analysis._**
	* **ARIMA**
		* _ARIMA is a model which is used for predicting future trends on a time series data. It is model that form of regression analysis._
		* _AR (Autoregression): Model that shows a changing variable that regresses on its own lagged/prior values._
		* _I (Integrated): Differencing of raw observations to allow for the time series to become stationary._
		* _MA (Moving average): Dependency between an observation and a residual error from a moving average model._
	* **prophet**
		* _Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well._
	* **SARIMA**
		* _Seasonal ARIMA is an extension of ARIMA that explicitly supports univariate time series data with a seasonal component. It adds three new hyperparameters to specify the autoregression (AR), differencing (I) and moving average (MA) for the seasonal component of the series, as well as an additional parameter for the period of the seasonality._

* **_Plotly graphing library used for explanatory data analysis & visualization._**
---

# Install the requirements
* Clone this repo (for help see this [tutorial](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/cloning-a-repository)).
* Install the requirements using `pip install -r requirements.txt`.
* Make sure you use Python 3.
* You may want to use a virtual environment for this.
---
# Pandas Profiling
_Click [**here**](https://jose-vincent.github.io/pandasProfileReport-/) to see the pandas profiling_

Pandas profiling save us all the work of visualizing and understanding the distribution of each variable. It generates a report with all the information easily available.The generated report contains warnings that appear at the beginning. It tells us the variables that contain NaN values, variables with many zeros, categorical variables with high cardinality, etc.

---
# Data visualization  
_Click [**here**](https://jose-vincent.gitlab.io/exploratory-data-analysis) to see the code with plotly interactive visualization_

|**Sample Data**|
|---|
|![Sample Data](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/1.%20Sample%20data.png)|

|**Reported cases over time**|
|---|
|![Reported cases over time](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/2.%20Reported%20cases%20over%20time.png)|
|_Reported cases of Dengue fever in Trivandrum district from 2013 to 2018. Most number of cases were reported in 2017. Also gender wise there is not much noticible difference._|

|**Pivot table**|
|---|
|![Pivot table](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/3.%20Pivot%20table.png)|
|_As mentioned above most number of cases were in 2017 with some months reaching 4 digit numbers._|

|**Reported cases in each year**|
|---|
|![Reported cases in each year](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/4.%20Reported%20cases%20in%20each%20year.png)|

|**Reported cases over time - Year Wise**|
|---|
|![Reported cases over time ](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/5.%20Reported%20cases%20over%20time%20-%20Year.png)|

|**Box plot of cases**|
|---|
|![Box plot of cases](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/6.%20Box%20plot%20of%20cases.png)|
|_More cases are reported in June, July, August, as the spread of dengue is usually associated with heat and the rainy season, since the Aedes mosquito often comes in contact with humans after breeding in exposed still water._|

|**Distribution of Gender**|
|---|
|![Distribution of Gender](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/7.%20Distribution%20of%20Gender.png)|
|_Of the reported cases 52.5% are male & 47% are females. In order ti check age and sex, are associated with the likelihood of exposure to Aedes aegypti we need to check the next plot._|

|**Cases in each age group**|
|---|
|![Cases in each age group ](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/11.%20Cases%20in%20each%20age%20group%20(%25).png)|
|_Most patients fall into age category below 20 (37%) with age category 20 - 40 (33%) coming second. Only 5% are above age 60. There is no significant difference between gender ratios, we can see a maximum diffrence of 4% that too in the age category below 20. So sex have not much impact on dengue spread. More cases of dengue are reported among teens & youngsters as it can be seen from age distribution patients below._|

|**Distribution of age**|
|---|
|![Distribution of age](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/8.%20Distribution%20of%20age.png).png)|

|**Top areas with most reported cases**|
|---|
|![Top 10 areas with most reported cases](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/9.%20Top%2010%20areas%20with%20most%20reported%20cases.png)|

|**Bar race plot** Check [here](https://jose-vincent.gitlab.io/exploratory-data-analysis)|
|---|
|![Bar race plot](https://gitlab.com/jose-vincent/timeseries_analysis-of-dengue_incidence-in-trivandrum/-/raw/master/Plots/12.%20Bar%20race%20plot.png)|
