# Описание проекта
Интернет-магазин «Викишоп» запускает новый сервис. 
Теперь пользователи могут редактировать и дополнять описания товаров, 
как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. 
Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию.

Требуется обучить модель классифицировать комментарии на позитивные и негативные. 
Исходные данные содержат разметку  токсичности правок.
Предполагается, что построенная модель будет иметь метрику качества F1 не меньше 0.75.

# Навыки и инструменты

- pandas
- matplotlib.pyplot
- nltk
- seaborn
- numpy
- tqdm.notebook
- nltk.corpus.stopwords
- wordcloud.WordCloud
- transformers.AutoModel
- transformers.AutoTokenizer
- sklearn.feature_extraction.text.CountVectorizer
- sklearn.feature_extraction.text.TfidfVectorizer
- sklearn.feature_extraction.text.TfidfTransformer
- sklearn.linear_model.LogisticRegression
- sklearn.neighbors.KNeighborsClassifier
- sklearn.svm.SVC
- sklearn.tree.DecisionTreeClassifier
- sklearn.model_selection.GridSearchCV
- sklearn.model_selection.RandomizedSearchCV
- sklearn.dummy.DummyClassifier
- sklearn.feature_selection.f_classif
- sklearn.feature_selection.SelectKBest
- sklearn.feature_selection.mutual_info_classif
- sklearn.inspection.permutation_importance
- sklearn.pipeline.Pipeline
- sklearn.metrics.accuracy_score
- sklearn.metrics.confusion_matrix
- sklearn.metrics.f1_score
- sklearn.metrics.ConfusionMatrixDisplay
- nltk.stem.WordNetLemmatizer
- nltk.tokenize.word_tokenize

# Общий вывод
Решение задачи проводилось двумя способами: с помощью нейронной сети BERT и без нее, используя величины TF-IDF в качестве входных признаков.

В первом способе сначала текстовые данные преобразовывались в числовые векторы-эмбеддинги с помощью предобученной модели "unitary/toxic-bert", а затем на основе полученных числовых признаков подбиралась оптимальная модель для задачи классификации.
Важной особенностью задачи был сильный дисбаланс классов: токсичных отзывов в исходной выборке была только десятая часть.
Оптимальная модель подобрана с помощью случайного поиска, на этапе тестирования наилучшая модель выдала метрику f1 0.94 - больше требуемой.

Во втором способе текст был очищен от ненужных симловов и стоп-слов и лемматизирован. Итоговый пайплайн включал в себя преобразование текста в матрицу числовых данных (CountVectorizer), преобразование в матрицу значений TF-IDF (TfidfTransformer) и модель логистической регресии.
С помощью GridSearchCV был произведен подбор гиперпараметров логистической регрессии. Наилучшая найденная модель выдала метрику f1 на тесте 0.76 - гораздо меньше, чем BERT, но формально она удовлетворяет требованиям.

Для найденной модели выведены слова, которые внесли наибольший вклад при классификации отзывов на нейтральные и токсичные.
