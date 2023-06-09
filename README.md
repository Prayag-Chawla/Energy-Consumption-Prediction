
## Weather and Energy Prediction 
Basically what we are doing here is that we are predicting the energy consumotion of a smart home nd we are predciting the weather conditions as well and similar parameters. Various plotting techniques and algorithms are used, and then by using a suitable model, we finally predict our final say and match it with the actual data to check the accuracy.

## Moving Average
Naive hypothesis: "tomorrow will be the same as today". However, instead of a model like y^t=yt−1
 (which is actually a great baseline for any time series prediction problems and sometimes is impossible to beat), we will assume that the future value of our variable depends on the average of its k
 previous values. Therefore, we will use the moving average.

## Exponential smoothing
Now, let's see what happens if we start weighting all available observations while exponentially decreasing the weights as we move further back in time. There exists a formula for exponential smoothing that will help us with this:

y^t=α⋅yt+(1−α)⋅y^t−1
 
Here the model value is a weighted average between the current true value and the previous model values. The  α
  weight is called a smoothing factor. It defines how quickly we will "forget" the last available true observation. The smaller  α
  is, the more influence the previous observations have and the smoother the series is.

Exponentiality is hidden in the recursiveness of the function -- we multiply by  (1−α)
  each time, which already contains a multiplication by  (1−α)
  of previous model values.
  
## Autoregressive Integrated Moving Average Model (ARIMA)
This acronym is descriptive, capturing the key aspects of the model itself. Briefly, they are:

AR: Autoregression. A model that uses the dependent relationship between an observation and some number of lagged observations.
I: Integrated. The use of differencing of raw observations (e.g. subtracting an observation from an observation at the previous time step) in order to make the time series stationary.
MA: Moving Average. A model that uses the dependency between an observation and a residual error from a moving average model applied to lagged observations.

## LSTM Model

Long Short-Term Memory Networks is a deep learning, sequential neural network that allows information to persist. It is a special type of Recurrent Neural Network which is capable of handling the vanishing gradient problem faced by RNN. LSTM was designed by Hochreiter and Schmidhuber that resolves the problem caused by traditional rnns and machine learning algorithms.
![image](https://github.com/Prayag-Chawla/Energy-Consumption-Prediction/assets/92213377/5a413cbf-01de-455d-9c6c-e02d6ac4ddf2)




## Usage and Installation

```
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

%matplotlib inline
from sklearn.metrics import r2_score, median_absolute_error, mean_absolute_error
from sklearn.metrics import median_absolute_error, mean_squared_error, mean_squared_log_error


from sklearn.model_selection import TimeSeriesSplit


```


## OUTPUT

![image](https://github.com/Prayag-Chawla/Energy-Consumption-Prediction/assets/92213377/c6788602-b51f-4f65-94cf-23a790319a18)
![image](https://github.com/Prayag-Chawla/Energy-Consumption-Prediction/assets/92213377/9d287524-7c0f-4084-9f9e-a868876010f6)
![image](https://github.com/Prayag-Chawla/Energy-Consumption-Prediction/assets/92213377/4c479ffe-5910-421f-9195-f5bde1173f6b)




## Used By
The project is used by various comapanies involving statistical approaches towards their customer proposition. Mostly used in the field of IoT related improvements in smart cities, the AI model can be exclusively used to track the energy consumed by households or even the businesses.
## Feedback

If you have any feedback, please reach out to us at chawlapc.619@gmail.com

