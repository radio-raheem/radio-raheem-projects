#  Прогнозирование заказов такси  
  
Сервис такси собрал исторические данные о заказах такси в аэропортах.  
Чтобы привлекать больше водителей в период пиковой нагрузки, нужно спрогнозировать количество заказов такси на следующий час.  
Нам нужно построить модель для такого предсказания.

Значение метрики *RMSE* на тестовой выборке должно быть не больше 48.

Нам нужно:

1. Загрузить данные и выполнить их ресемплирование по одному часу.
2. Проанализировать данные.
3. Обучить разные модели с различными гиперпараметрами. Сделать тестовую выборку размером 10% от исходных данных.
4. Проверить данные на тестовой выборке и сделать выводы.


Данные лежат в файле `taxi.csv`.  
Количество заказов находится в столбце `num_orders` (от англ. *number of orders*, «число заказов»).  

Проект выполнен в **Jupyter Notebook**, версия сервера блокнотов: 6.1.4. Версия **Python** 3.7.8.
В проекте использованы библиотеки: 
* **Pandas**
* **NumPy**
* **statsmodels**
* **scikit-learn**
* **MatPlotLib**
* **Light GBM**
* **IPython**