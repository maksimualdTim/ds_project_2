
![](./images/data_cleaning.png)
# <center> Проект: Анализ резюме из HeadHunter </center>
## Оглавление
1. [Описание проекта](#Описание-проекта)
2. [Описание данных](#Описание-данных)
3. [Зависимости](#Зависимости)
4. [Установка проекта](#Установка-проекта)
5. [Использование проекта](#Использование-проекта)
6. [Выводы](Использование-проекта)

## Описание проекта

Проект для кадрового агентства, которое подбирает вакансии для IT-специалистов. Первый проект — создание модели машинного обучения, которая будет рекомендовать вакансии клиентам агентства, претендующим на позицию Data Scientist. Сначала необходимо понять, что из себя представляют данные и насколько они соответствуют целям проекта. В литературе эта часть работы над ML-проектом называется Data Understanding, или анализ данных.

**Основные этапы работы над проектом:**
* знакомство с данными;
* предварительный анализ данных;
* детальный анализ вакансий;
* анализ работодателей;
* предметный анализ.

**О структуре проекта:**
* [Project_2.ipynb](./Project_2.ipynb) - jupyter-ноутбук, содержащий основной код проекта


## Описание данных
![База данных](/resources/data.png)

Познакомимся с каждой таблицей.

# vacancies
Таблица хранит в себе данные по вакансиям и содержит следующие столбцы:

![Вакансии](/resources/vacancies.png)

Зарплатная вилка — это верхняя и нижняя граница оплаты труда в рублях (зарплаты в других валютах уже переведены в рубли). Соискателям она показывает, в каком диапазоне компания готова платить сотруднику на этой должности.

# areas

Таблица-справочник, которая хранит код региона и его название.

![Регионы](/resources/areas.png)

# employers

Таблица-справочник со списком работодателей.

![Работодатели](/resources/employers.png)

# industries

Таблица-справочник вариантов сфер деятельности работодателей.

![Сферы деятельности](/resources/industries.png)

# employers_industries

Дополнительная таблица, которая существует для организации связи между работодателями и сферами их деятельности.

Эта таблица нужна нам, поскольку у одного работодателя может быть несколько сфер деятельности (или работодатели могут вовсе не указать их). Для удобства анализа необходимо хранить запись по каждой сфере каждого работодателя в отдельной строке таблицы.

![Вспомогательная таблица для  связи](/resources/employers_industries.png)

## Используемые зависимости
* Python:
    * [psycopg2](https://pypi.org/project/psycopg2/)
    * [pandas](https://pandas.pydata.org)
    * [plotly](https://plotly.com/)
    * [seaborn](https://seaborn.pydata.org)

## Установка проекта

```
git clone https://github.com/maksimualdTim/ds_project1_headhunter.git
```
Заполнить данные для подключения к базе данных впервой ячейке jupyter-ноутбука.

## Использование
Вся информация о работе представлена в jupyter-ноутбуке Project_2.ipynb.

## Выводы

В данной работе был произведен анализ данных hh.ru по вакансиям.