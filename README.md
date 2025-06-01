# ML-моделирование биологических активностей

## Структура проекта

| Файл                                           | Назначение                                                                  |
|------------------------------------------------|-----------------------------------------------------------------------------|
| `course_work_ml.xlsx`                          | Основной датасет с химическими дескрипторами и биологическими метриками     |
| `processed_data.xlsx`                          | Датасет после EDA                                                           |
| `course_work_ML_Voronin_Regression_IC50.ipynb` | Jupyter Notebook: Регрессия для IC50 подбором гиперпараметров               |
| `course_work_ML_Voronin_Regression_SI.ipynb`   | Jupyter Notebook: Регрессия для SI подбором гиперпараметров                 |
| `course_work_ML_Voronin_Regression_СС50.ipynb` | Jupyter Notebook: Регрессия для CC50 подбором гиперпараметров               |
| `course_work_ML_Voronin_Classifier_IC50.ipynb` | Jupyter Notebook: Классификация IC50 по медиане                             |
| `course_work_ML_Voronin_Classifier_СС50.ipynb` | Jupyter Notebook: Классификация CC50 по медиане                             |
| `course_work_ML_Voronin_Classifier_SI.ipynb`   | Jupyter Notebook: Классификация SI по медиане                               |
| `course_work_ML_Voronin_Classifier_SI_2.ipynb` | Jupyter Notebook: Классификация SI по порогу 8                              |
| `Аналитический отчет.pdf`               | Аналитический отчёт о проделанной работе и рекомендациями                   |

## Основные задачи

- Регрессия:
  - `IC50` 
  - `CC50`
  - `SI`
- Классификация:
  - Превышает ли значение медиану (`IC50`, `CC50`, `SI`)
  - Превышает ли `SI` порог 8

## Используемые технологии

- Python (pandas,numpy, sklearn, xgboost, matplotlib)
- Feature Selection: `SelectKBest`, `mutual_info_*`
- Модели: `XGBoost`, `RandomForest`, `LogisticRegression`, `KNN`, `LinearRegression`,`Ridge`,`Lasso`

## Результаты

-	XGBoost показал высокую эффективность в задачах регрессии и большинстве задач классификации, что делает его лучшим выбором
-	Для задачи Si > 8, лучше взять обычную логистическую регрессию
-	Рекомендуется логарифмировать все целевые значения перед обучения, чтобы стабилизировать обучение и повысить точность
-	В задачах классификации можно использовать ансамбль моделей, например XGBoost и Logistic Regression, чтобы повысить устойчивость предсказаний
-	Несмотря на высокую точность XGBoost, в задачах где критично интерпретируемость, стоит взять logistic regression и RandomForest

---

