This is an ongoing project in world covid19 data analysis.The tool used is MS Excel. We use the daily new infections in China as a case study. We tried to analyze the data in two ways.

In the first method, we plot the daily timeseries and use the Forecast.ETS inbuilt function in Excel to make a prediction of the daily cases for a period of three months.
 
In the second method, we used the SIR model for spread of infectious disease transmission. The SIR Model is implemented using Euler's method. Now we calibrate this model by estimating the parameters infection rate(denoted by beta) and recovery rate(denoted by gamma) from the available covid19 data of China. The daily new cases data for Shanghai city during the initial exponential growth stage from March 1st 2022 to April 14 2022 is used. We estimate the SIR Model parameters from this data using least square statistics. First the fitting was done on daily new cases data and parameters were estimated. Then the fitting was done on daily cumulative cases data and parameters were estimated. The slope of the best fit line gives the difference (Beta-Gamma) of parameters infection rate(Beta) and recovery rate(Gamma). Now we can easily determine recovery rate by assuming a suitable infectious period as recovery rate is usually taken as the reciprocal of infectious period. After that we can easily calculate infection rate(Beta) and the basic reproduction ratio. The estimated values of the parameters can be used in the SIR Model to predict the time series of active cases.

Infectious cases in SIR Model represents the active cases(prevalent cases) daily. So fitting the model to the active cases might give a more reasonable estimate of the parameters. But the data of active cases is usually not available. So the daily cumulative cases may be considered as a good approximation of daily actual cases atleast during the initial exponential growth phase. 

This is only a preliminary analysis. We intend to do more as we learn more tools.
 
Reference:
https://pubmed.ncbi.nlm.nih.gov/32834642/