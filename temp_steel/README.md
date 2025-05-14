Температура сплава на этапе обработки стали

Чтобы оптимизировать производственные расходы, 
металлургическому комбинату требуется уменьшить потребление электроэнергии на этапе обработки стали.
Для этого комбинату нужно контролировать температуру сплава. 

Задача состоит в построении модели, которая будет её предсказывать. 
Разработанная модель будет использована для имитации технологического процесса.

Навыки и инструменты
python
pandas
numpy
scipy
matplotlib
sklearn.model_selection.cross_val_score
sklearn.metrics.mean_squared_error
sklearn.metrics.mean_absolute_error
sklearn.preprocessing.StandardScaler
sklearn.pipeline.Pipeline
sklearn.compose.ColumnTransformer
sklearn.linear_model.LinearRegression
sklearn.linear_model.SGDRegressor
sklearn.tree.DecisionTreeRegressor
sklearn.tree.DecisionTreeClassifier
sklearn.model_selection.RandomizedSearchCV
sklearn.dummy.DummyRegressor
catboos.CatBoostRegressor
sklearn.feature_selection.SelectKBest

Общий вывод
Проведен выбор наилучшей модели случайным поиском с кросс-валидацией и подбором гиперпараметров среди линейной регрессии, DecisionTreeRegressor, SGDRegressor и CatBoostRegressor. Выбранная модель соответствует требуемым критериям по метрике МАЕ на тестовом наборе. Отбор признаков был произведен во время поиска наилучшей модели методом SelectKBest. 
