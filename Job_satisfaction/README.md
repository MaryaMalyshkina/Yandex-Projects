# Описание проекта
HR-аналитики компании «Работа с заботой» помогают бизнесу оптимизировать управление персоналом: 
бизнес предоставляет данные, а аналитики предлагают, как избежать финансовых потерь и оттока сотрудников.

Компания предоставила данные с характеристиками сотрудников компании. 
Среди них — уровень удовлетворённости сотрудника работой в компании. 
Эту информацию получили из форм обратной связи: сотрудники заполняют тест-опросник, 
и по его результатам рассчитывается доля их удовлетворённости от 0 до 1, 
где 0 — совершенно неудовлетворён, 1 — полностью удовлетворён.

Первая задача — построить модель, которая сможет предсказать уровень удовлетворённости 
сотрудника на основе данных заказчика. Выбор должен быть сделан на основе метрики SMAPE.

Вторая задача — построить модель, которая сможет на основе данных заказчика 
предсказать то, что сотрудник уволится из компании.
# Навыки и инструменты

- pandas
- matplotlib.pyplot
- seaborn
- numpy
- phik
- scipy
- sklearn.linear_model.LinearRegression
- sklearn.linear_model.LogisticRegression
- sklearn.neighbors.KNeighborsClassifier
- sklearn.svm.SVC
- sklearn.tree.DecisionTreeClassifier
- sklearn.tree.DecisionTreeRegressor
- sklearn.model_selection.RandomizedSearchCV
- sklearn.model_selection.cross_val_score
- sklearn.feature_selection.SelectKBest
- sklearn.dummy.DummyClassifier
- sklearn.preprocessing.StandardScaler
- sklearn.preprocessing.OneHotEncoder
- sklearn.preprocessing.OrdinalEncoder
- sklearn.preprocessing.MinMaxScaler
- sklearn.preprocessing.LabelEncoder
- sklearn.preprocessing.PolynomialFeatures
- sklearn.impute.SimpleImputer 
- sklearn.metrics.roc_auc_score
- sklearn.metrics.make_scorer
- sklearn.pipeline.Pipeline
- sklearn.compose.ColumnTransformer

# Общий вывод

предобработку данных, в результате которой были устранены пропуски в данных,
исследовательский анализ, включая корреляционный, для визуализации входных и целевого признака и нахождения взаимосвязей между ними,
подготовку данных (категорирование и масштабирование признаков),
поиск наилучшей модели для прогнозирования уровня удовлетворенности работой, подбор гиперпараметров, и отбор наилучших признаков.
Найденная модель соответствует критерию успеха по метрике smape, сравнение с константной моделью показало ее адекватность.
