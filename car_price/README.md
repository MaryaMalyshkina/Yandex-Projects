# Описание проекта
Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает 
приложение для привлечения новых клиентов, в котором можно быстро узнать 
рыночную стоимость своего автомобиля.

Проект посвящен построению модели для определения 
стоимости на основе входящих признаков: год регистрации автомобиля, марка, модель, 
мощность двигателя, тип кузова и коробки передач, пробег, вид топлива, 
почтовый индекс владельца, дата скачивания анкеты из базы.

# Навыки и инструменты
- pandas
- matplotlib.pyplot
- seaborn
- numpy
- phik
- time
- shap
- scipy.stats
- sklearn.linear_model.LinearRegression
- sklearn.preprocessing.StandardScaler
- sklearn.preprocessing.OneHotEncoder
- sklearn.preprocessing.OrdinalEncoder
- sklearn.impute.SimpleImputer
- sklearn.metrics.mean_squared_error
- sklearn.pipeline.Pipeline
- sklearn.compose.ColumnTransformer
- catboost.CatBoostRegressor
- lightgbm.LGBMRegressor
- sklearn.linear_model.SGDRegressor
- sklearn.tree.DecisionTreeClassifier
- sklearn.tree.DecisionTreeRegressor
- sklearn.model_selection.RandomizedSearchCV
- sklearn.model_selection.cross_val_score
- sklearn.inspection.permutation_importance
- shap.Explanation



# Общий вывод
Рассмотрены четыре различные модели: DecisionTreeRegressor, SGDRegressor, CatBoost и LightGBM.

Для каждой модели с помощью случайного поиска с кросс-валидацией на 5 выборках проведен подбор гиперпараметров.
Выбор наилучшей модели произведен на основе сравнения валидационных метрик RSME. 

Для лучшей модели проведен анализ остатков.

С помощью метода permutation_importance и SHAP выявлены признаки, наиболее значимые для модели.
