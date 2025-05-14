# Описание проекта
Компания «Чётенькое такси» собрала исторические данные о заказах такси в аэропортах. 

Чтобы привлекать больше водителей в период пиковой нагрузки, 
нужно спрогнозировать количество заказов такси на следующий час. 

Необходимо построить модель для такого предсказания.

# Навыки и инструменты
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
import os
import time
import lightgbm as  lgb
import statsmodels
import skforecast

from matplotlib import rcParams
from scipy import stats as st
from sklearn.linear_model import (
    LinearRegression,
    LogisticRegression
)

from sklearn.model_selection import train_test_split

from sklearn.metrics import (
    mean_squared_error,
    root_mean_squared_error,
)
    
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import cross_val_score
from sklearn.tree import DecisionTreeRegressor
from sklearn.model_selection import GridSearchCV

from sklearn.model_selection import TimeSeriesSplit

from pmdarima import auto_arima
from prophet import Prophet
from statsmodels.graphics.tsaplots import plot_acf
from statsmodels.tsa.stattools import adfuller
from statsmodels.tsa.arima_model import ARIMA
from statsmodels.tsa.arima.model import ARIMA
from statsmodels.tsa.seasonal import seasonal_decompose
from skforecast.recursive import ForecasterSarimax
from statsmodels.tsa.statespace.sarimax import SARIMAX
from skforecast.sarimax import Sarimax
from skforecast.recursive import ForecasterSarimax
from skforecast.model_selection import TimeSeriesFold
from skforecast.model_selection import grid_search_sarimax


# Общий вывод

