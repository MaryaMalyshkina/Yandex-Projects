# Описание проекта
Компания собрала исторические данные о заказах такси в аэропортах. 

Чтобы привлекать больше водителей в период пиковой нагрузки, 
нужно спрогнозировать количество заказов такси на следующий час. 

Необходимо построить модель для такого предсказания.

# Навыки и инструменты
- pandas
- matplotlib
- seaborn
- numpy
- statsmodels
- skforecast
- scipy.stats
- statsmodels.graphics.tsaplots.plot_acf
- sklearn.model_selection.TimeSeriesSplit
- sklearn.linear_model.LinearRegression
- sklearn.metrics.root_mean_squared_error
- sklearn.tree.DecisionTreeClassifier
- sklearn.tree.DecisionTreeRegressor
- sklearn.model_selection.GridSearchCV
- prophet.Prophet




from pmdarima import auto_arima

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

