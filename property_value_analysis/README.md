### Описание проекта
* Данные сервиса Яндекс Недвижимость — архив объявлений за несколько лет о продаже квартир в Санкт-Петербурге и соседних населённых пунктах.* 
* Ваша задача — выполнить предобработку данных и изучить их, чтобы найти интересные особенности и зависимости, которые существуют на рынке недвижимости.
### Задачи 
Шаг 1. Откройте файл с данными и изучите общую информацию

Загрузите данные из файла в датафрейм.
Изучите общую информацию о полученном датафрейме.
Постройте общую гистограмму для всех числовых столбцов таблицы. Например, для датафрейма data это можно сделать командой data.hist(figsize=(15, 20)).


Шаг 2. Предобработка данных
* Найдите и изучите пропущенные значения в столбцах:
* Определите, в каких столбцах есть пропуски.
* Заполните пропущенные значения там, где это возможно. 
* Найдите столбцы, в которых нужно изменить тип данных.
* Преобразуйте тип данных в выбранных столбцах.
* Изучите уникальные значения в столбце с названиями и устраните неявные дубликаты. 
* Найдите и устраните редкие и выбивающиеся значения. Например, в столбце ceiling_height может быть указана высота потолков 25 м и 32 м. Логично предположить, что на самом деле это вещественные значения: 2.5 м и 3.2 м. 
* Если природа аномалии понятна и данные действительно искажены, то восстановите корректное значение. В противном случае удалите редкие и выбивающиеся значения.

Шаг 3. Добавьте в таблицу новые столбцы со следующими параметрами:
* цена одного квадратного метра;
* день недели публикации объявления (0 — понедельник, 1 — вторник и так далее);
* месяц публикации объявления;
* год публикации объявления;
* тип этажа квартиры (значения — «‎первый», «последний», «другой»);
* расстояние до центра города в километрах (переведите из м в км и округлите до целых значений).


Шаг 4. Проведите исследовательский анализ данных:
Изучите следующие параметры объектов: общая площадь, жилая площадь, площадь кухни, цена объекта, количество комнат, высота потолков, этаж квартиры, тип этажа квартиры («первый», «последний», «другой»); общее количество этажей в доме, расстояние до центра города в метрах, расстояние до ближайшего аэропорта, расстояние до ближайшего парка, день и месяц публикации объявления.

* Постройте отдельные гистограммы для каждого из этих параметров. Опишите все ваши наблюдения по параметрам в ячейке с типом markdown.
* Изучите, как быстро продавались квартиры (столбец days_exposition). Этот параметр показывает, сколько дней было размещено каждое объявление. 
 
* Постройте гистограмму.
* Посчитайте среднее и медиану.

* Изучите, зависит ли цена от: общей площади, жилой площади, площади кухни, количества комнат, этажа (первый, последний, другой), даты размещения (день недели, месяц, год).
* Постройте графики, которые покажут зависимость цены от указанных выше параметров. Для подготовки данных перед визуализацией вы можете использовать сводные таблицы.
* Посчитайте среднюю цену одного квадратного метра в 10 населённых пунктах с наибольшим числом объявлений. Выделите населённые пункты с самой высокой и низкой стоимостью квадратного метра. Эти данные можно найти по имени в столбце locality_name.

* Ранее вы посчитали расстояние до центра в километрах. Теперь выделите квартиры в Санкт-Петербурге с помощью столбца locality_name и вычислите среднюю цену каждого километра. Опишите, как стоимость объектов зависит от расстояния до центра города.



Шаг 5. Напишите общий вывод
Опишите полученные результаты и зафиксируйте основной вывод проведённого исследования.