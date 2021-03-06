# Выбор локации для скважины  
  
Вы работаете в нефтедобывающей компании. Нужно решить, где бурить новую скважину.  

Вам предоставлены пробы нефти в трёх регионах: в каждом 10 000 месторождений, где измерили качество нефти и объём её запасов. Постройте модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль.
Шаги для выбора локации:
  
Основными этапами нашего проекта станут:

* Загрузка и подготовка данных
* Обучение и проверка модели
* Подготовка к расчёту прибыли
* Расчёт прибыли и рисков. Выбор региона для разработки месторождений

**Описание данных**

*Признаки*  
  
*id* — уникальный идентификатор скважины  
*f0, f1, f2* — три признака точек (нам неизвестно, что они означают, но сами признаки значимы)  
  
*Целевой признак*  
  
**product** — объём запасов в скважине (тыс. баррелей)  
  
Условия задачи:
Для обучения модели подходит только линейная регрессия (остальные — недостаточно предсказуемые).  
При разведке региона исследуют 500 точек, из которых с помощью машинного обучения выбирают 200 лучших для разработки.  
Бюджет на разработку скважин в регионе — 10 млрд рублей.  
При нынешних ценах один баррель сырья приносит 450 рублей дохода. Доход с каждой единицы продукта составляет 450 тыс. рублей, поскольку объём указан в тысячах баррелей.  
После оценки рисков нужно оставить лишь те регионы, в которых вероятность убытков меньше 2.5%. Среди них выбирают регион с наибольшей средней прибылью.
  
Проект выполнен в **Jupyter Notebook**, версия сервера блокнотов: 6.1.4. Версия **Python** 3.7.8.
В проекте использованы библиотеки:
* **Pandas**
* **NumPy**
* **SciPy**
* **scikit-learn**
* **IPython**
