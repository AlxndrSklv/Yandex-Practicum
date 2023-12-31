# [Прогнозирование заказов такси](https://github.com/AlxndrSklv/Yandex-Practicum/blob/3fd08dece14461d5e1843a86930515fe6ee9745b/Taxi_orders_forcast/Taxi_orders_forcast.ipynb)

## Описание проекта

Требуется построить модель с целью прогноза количества заказов такси на следующий час, чтобы привлекать больше водителей в период пиковой нагрузки. Значение метрики RMSE на тестовой выборке должно быть не больше 48.

## Описание данных

Данные лежат в файле taxi.csv.

Количество заказов находится в столбце 'num_orders'.

## Навыки и инструменты

Python, Pandas, Lightgbm, Matplotlib, NumPy, Catboost, Scikit-learn исследовательский анализ данных

- import sklearn

- import pandas as pd
- import numpy as np
- import matplotlib.pyplot as plt
- import lightgbm as lgb

- from sklearn.model_selection import train_test_split
- from sklearn.linear_model import LinearRegression
- from sklearn.metrics import mean_squared_error
- from sklearn.model_selection import GridSearchCV
- from sklearn.ensemble import RandomForestRegressor
- from sklearn.model_selection import RandomizedSearchCV
- from statsmodels.tsa.seasonal import seasonal_decompose
- from sklearn.model_selection import TimeSeriesSplit
- from catboost import CatBoostRegressor
- from lightgbm import LGBMRegressor

## Общий вывод

Проведено исследование временного ряда на предмет трендовых и сезонных закономерностей, случайной составляющей. Для обучения инициализировали 4 модели LinearRegression, RandomForestRegressor, LGBMRegressor, CatBoostRegressor. Кроме LinearRegression значения RMSE у всех моделей меньше требуемых 48. Из всех рассмотренных моделей выбар пал на CatBoostRegressor, тк у нее лучшее значение RMSE на тестовой выборке (RMSE 41) и обучение занимает относительно малое время (2 мин 22 сек).
