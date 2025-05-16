# Описание проекта
Прогноз снижения покупательской активности интернет-магазина «В один клик»

Отчёт магазина «В один клик» за прошлый период показал, 
что активность покупателей начала снижаться.

Нужно построить модель, которая предскажет вероятность 
снижения покупательской активности клиента в следующие три месяца.

Используя данные модели и данные о прибыльности клиентов,
нужно выделить сегменты покупателей и разработать для них 
персонализированные предложения.
# Навыки и инструменты

- pandas
- matplotlib.pyplot
- seaborn
- numpy
- scipy
- phik
- SHAP
- sklearn.metrics.roc_auc_score
- sklearn.preprocessing.StandardScaler
- sklearn.preprocessing.OneHotEncoder
- sklearn.preprocessing.OrdinalEncoder
- sklearn.preprocessing.MinMaxScaler
- sklearn.pipeline.Pipeline
- sklearn.compose.ColumnTransformer
- sklearn.linear_model.LogisticRegression
- sklearn.neighbors.KNeighborsClassifier
- sklearn.svm.SVC  
- sklearn.tree.DecisionTreeClassifier
- sklearn.model_selection.RandomizedSearchCV
- sklearn.model_selection.cross_val_score
- sklearn.inspection.permutation_importance

# Общий вывод
Предсказание покупательской активности представляет собой задачу классификации.
Модели, которые использовались в решении: KNeighborsClassifier, DecisionTreeClassifier, SVC и LogisticRegression.

Для поиска лучшей модели использовался случайный поиск: перебирались и модели, и их гиперпараметры, и методы подготовки данных.
При поиске использовалась ROC-AUC, поскольку она универсальна при всех возможных значениях порогов.
Лучшей моделью оказалась логистическая регрессия с масштабированием количественных признаков с помощью MinMaxScaler().

Отбор наиболее важных признаков для лучшей модели произведен двумя методами: permutation importance и SHAP.
По результатам анализа важности признаков среднее число просмотренных страниц за визит является сильно значимым признаком для модели, и по этому признаку проведена сегментация покупателей.
