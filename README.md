# House Prices
## Задача
Создать модель, прогнозирующую стоимость домов, на основе его признаков с использованием нескольких моделей обучения. Задание взято с [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/overview).

## Решение задачи
1. Смотрим на распределение цены и логарифмируем её для приведения к нормальному виду.
2. Удаляем признак ID, разбиваем наши выборки на строковые и числовые. Добавляем несколько новых признаков. Заполняем пропущенные значения.
3. Проводим предварительное обучение с помощью XGBRegressor для заполнения целевой переменной в тестовой выборке.
4. Соединяем выборки и проводим кластеризацию, результат которой добавляем, как новый признак.
5. Производим Label Encoding с некоторыми категориальными переменными. Производим One Hot Encoding по всем строковым переменным.
6. Разделяем общую выборку на train и test.
7. Обучаем 4 модели:
    * RandomForestRegressor
    * XGBRegressor
    * LGBMRegressor
    * CatBoostRegressor
8. Выбираем лучшую модель и смотрим feature importances. Далее сохраняем результаты в новый файл и загружаем на [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/overview).
