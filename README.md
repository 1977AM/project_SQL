# Проект SQL

### Описание проекта

Создание модели машинного обучения, которая будет рекомендовать вакансии клиентам агентства, претендующим на позицию Data Scientist

## Наш проект включает в себя несколько этапов:
1. Знакомство с данными
2. Предварительный анализ данных
3. Детальный анализ вакансий
4. Анализ работодателей
5. Предметный анализ
6. Общий вывод по проекту



### Знакомство с данными
Познакомимся с каждой таблицей.

VACANCIES

Таблица хранит в себе данные по вакансиям и содержит следующие столбцы:

id - ID вакансии
name - Название вакансии
key_skills - Ключевые навыки
schedule - Тип рабочего графика
experience - Требования к опыту
employment - Тип трудоустройства
salary_from - Нижняя граница зарплатной вилки
salary_to - Верхняя граница зарплатной вилки
area_id - ID региона работадателя
exployer_id - ID работадателя


Зарплатная вилка — это верхняя и нижняя граница оплаты труда в рублях (зарплаты в других валютах уже переведены в рубли). Соискателям она показывает, в каком диапазоне компания готова платить сотруднику на этой должности.

AREAS

Таблица-справочник, которая хранит код региона и его название.

id - Идентификатор города
name - Название города

EMPLOYERS

Таблица-справочник со списком работодателей.

id - Номер работадателя
name - Название работадателя
area - Регион регистрации

INDUSTRIES

Таблица-справочник вариантов сфер деятельности работодателей.

id - ID сферы деятельности
name - Название сферы деятельности

EMPLOYERS_INDUSTRIES

Дополнительная таблица, которая существует для организации связи между работодателями и сферами их деятельности.

Эта таблица нужна нам, поскольку у одного работодателя может быть несколько сфер деятельности (или работодатели могут вовсе не указать их). Для удобства анализа необходимо хранить запись по каждой сфере каждого работодателя в отдельной строке таблицы.

employer_id - ID работадателя
industry_id - ID сферы деятельности


# Общий вывод по проекту

Ресурс  HH.ru востребован, в нем широко представлены регионы, работадатели, вакансии.
Количество работадателей и вакансий, конечно, зависит от количество жителей региона, населенного пункта. Везде лидер - Москва. 
Самый популярный график - полный рабочий день с полной занятостью и, соответственно, максимально возможной з/п. Всё большую популярность набирает график с удаленной работой, но полной занятостью.
Работадатели готовы брать людей с опытом от года. Навыки есть, з/п не максимальная.
Работадателям можно посоветовать указывать сферу деятельности. Так эффективней искать претендентов.
Наибольшее количество вакансий у "цифровых" компаний, в частности Яндекса. Этот тренд будет только усиливаться. Большое количество вакансий за программистами. Есть своя доля и у data scientist. Уровень з/п у них высокий и быстро растет с опытом. 
