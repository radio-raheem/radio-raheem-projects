# Предсказание температуры сплава  
Чтобы оптимизировать производственные расходы, металлургический комбинат решил уменьшить потребление электроэнергии на этапе обработки стали. Нам нужно построить модель, которая предскажет температуру стали.  

## Описание производственного процесса
Сталь обрабатывают в металлическом ковше вместимостью около 100 тонн. Чтобы ковш выдерживал высокие температуры, изнутри его облицовывают огнеупорным кирпичом. Расплавленную сталь заливают в ковш и подогревают до нужной температуры графитовыми электродами. Они установлены в крышке ковша.
Из сплава выводится сера (десульфурация), добавлением примесей корректируется химический состав и отбираются пробы. Сталь легируют — изменяют её состав — подавая куски сплава из бункера для сыпучих материалов или проволоку через специальный трайб-аппарат (англ. tribe, «масса»).
Перед тем как первый раз ввести легирующие добавки, измеряют температуру стали и производят её химический анализ. Потом температуру на несколько минут повышают, добавляют легирующие материалы и продувают сплав инертным газом. Затем его перемешивают и снова проводят измерения. Такой цикл повторяется до достижения целевого химического состава и оптимальной температуры плавки.
Тогда расплавленная сталь отправляется на доводку металла или поступает в машину непрерывной разливки. Оттуда готовый продукт выходит в виде заготовок-слябов (англ. slab, «плита»).  
  
## Описание данных  

Данные состоят из файлов, полученных из разных источников:

- `data_arc.csv` — данные об электродах;
- `data_bulk.csv` — данные о подаче сыпучих материалов (объём);
- `data_bulk_time.csv` *—* данные о подаче сыпучих материалов (время);
- `data_gas.csv` — данные о продувке сплава газом;
- `data_temp.csv` — результаты измерения температуры;
- `data_wire.csv` — данные о проволочных материалах (объём);
- `data_wire_time.csv` — данные о проволочных материалах (время).

Во всех файлах столбец `key` содержит номер партии. В файлах может быть несколько строк с одинаковым значением `key`: они соответствуют разным итерациям обработки.

## Примерный план решения задачи

1. Изучение данных
2. Исследовательский анализ данных
3. Подготовка данных. Объединение таблиц
4. Подготовка признаков
5. Проверка признаков на мультиколлинеарность
6. Разбиение датасета на тренировочный и тестовый наборы
7. Создание модели. Подбор гиперпараметров с помощью кросс-валидации
8. Тестирование модели
9. Анализ важности признаков у модели
10. Проверка модели на вменяемость

Проект выполнен в **Jupyter Notebook**, версия сервера блокнотов: 6.4.6.  
Версия **Python** 3.10.1.  
В проекте использованы библиотеки:  
* **Pandas**
* **NumPy** 
* **Seaborn** 
* **MatPlotLib** 
* **statsmodel** 
* **scikit-learn**
* **модуль IPython**
* **Light GBM**
