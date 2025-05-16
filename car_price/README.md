# Описание проекта
Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает 
приложение для привлечения новых клиентов, в котором можно быстро узнать 
рыночную стоимость своего автомобиля.

Проект посвящен построению модели для определения 
стоимости на основе входящих признаков: год регистрации автомобиля, марка, модель, 
мощность двигателя, тип кузова и коробки передач, пробег, вид топлива, 
почтовый индекс владельца, дата скачивания анкеты из базы.

# Навыки и инструменты
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
import phik
import os
import time
import lightgbm as  lgb
import shap

from matplotlib import rcParams
from scipy import stats as st
from sklearn.linear_model import (
    LinearRegression,
    LogisticRegression
)

from sklearn.preprocessing import (
    StandardScaler,
    OneHotEncoder,
    OrdinalEncoder,
    MinMaxScaler
)

from sklearn.model_selection import train_test_split
from sklearn.impute import SimpleImputer

from sklearn.metrics import (
    mean_squared_error,
    root_mean_squared_error
)

from sklearn.pipeline import Pipeline
from sklearn.compose import ColumnTransformer

from catboost import CatBoostRegressor
from lightgbm import LGBMRegressor
from sklearn.linear_model import SGDRegressor
from sklearn.tree import DecisionTreeClassifier, DecisionTreeRegressor
from sklearn.model_selection import RandomizedSearchCV
from sklearn.model_selection import cross_val_score

from sklearn.inspection import permutation_importance
from shap import Explanation
from shap.plots import waterfall, beeswarm
from sklearn.feature_selection import SelectKBest, f_regression


# Общий вывод
Рассмотрены четыре различные модели: DecisionTreeRegressor, SGDRegressor, CatBoost и LightGBM.

Лучшей по метрике оказалась LightGBM, а по времени обучения и предсказания - DecisionTreeRegressor.
Самый простой показатель для оценки важности признаков в моделях без встроенных весов является permutation importance, «важность после перестановки». Его применим к нашей лучшей модели.
Наибольшую важность для модели имеют признаки: год регистрации, мощность двигателя и модель. Наименее важные - тип топлива и коробка передач.
