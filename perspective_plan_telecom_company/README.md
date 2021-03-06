# Определение перспективного тарифа для телеком-компании

Нашей задачей является предварительный анализ тарифов сотовой связи телеком-компании на небольшой выборке клиентов. В нашем распоряжении данные 500 пользователей: кто они, откуда, каким тарифом пользуются, сколько звонков и сообщений каждый отправил за 2018 год. Нужно проанализировать поведение клиентов и сделать вывод — какой тариф лучше. На основании этого вывода коллеги из коммерческого департамента компании скорректируют рекламный бюджет.  
Основными этапами нашего проекта станут:  
* Изучение предоставленных данных
* Предобработка данных
* Расчеты и добавление необходимых для анализа результатов
* Анализ данных
* Проверка гипотез
* Формулирование основных выводов

Проект выполнен в Jupyter Notebook, версия сервера блокнотов: 6.1.4. Версия Python 3.7.8.  
В проекте использованы библиотеки Pandas, MatPlotLib, NumPy, Math, SciPy, а также модуль IPython. 


# Описание тарифов

**Тариф «Смарт»**

1. Ежемесячная плата: 550 рублей
2. Включено 500 минут разговора, 50 сообщений и 15 Гб интернет-трафика
3. Стоимость услуг сверх тарифного пакета: 1. минута разговора: 3 рубля (Телеком-компания всегда округляет вверх значения минут и мегабайтов. Если пользователь проговорил всего 1 секунду, в тарифе засчитывается целая минута); 2. сообщение: 3 рубля; 3. 1 Гб интернет-трафика: 200 рублей.

**Тариф «Ультра»**
1. Ежемесячная плата: 1950 рублей
2. Включено 3000 минут разговора, 1000 сообщений и 30 Гб интернет-трафика
3. Стоимость услуг сверх тарифного пакета: 1. минута разговора: 1 рубль; 2. сообщение: 1 рубль; 3. 1 Гб интернет-трафика: 150 рублей.
