# Action Probability

Задча предсказания вероятности действия пользователя по существующим признакам.

## Описание кейса

Файл person содержит всех уникальных людей (и соответствующие характеристики), которые выполняли действия с течением времени. Каждая строка в файле представляет уникального человека. У каждого человека есть уникальный person_id.

Файл action_train содержит все уникальные действия (и соответствующие характеристики действий), которые каждый человек выполнял в течение определенного времени. Каждая строка в файле действий представляет собой уникальное действие, выполненное человеком в определенный день. Каждое действие имеет уникальный идентификатор action_id. В файле содержится несколько различных категорий действий. Действия типа 1 отличаются от действий типа 2-7, поскольку известно больше характеристик, связанных с действиями типа 1 (всего девять), чем с действиями типа 2-7 (которые имеют только одну связанную характеристику).

## Задача

Задача состоит в том, чтобы для каждого action_id в action_test предсказать result как float от 0 до 1.

## Решение

* Знакомство с данными, EDA.
* Работа с пропусками.
* Сегментация объектов по типу действия.
* Построение разных моделей в зависимости от типа действия.
* Оценка качества на валидацонной выборке.
* Выводы

## Данные

Table user_data.  
Contains information about all users of the social network.

|        Field name      |                         Overview                         |
|------------------------|----------------------------------------------------------|
| Deal_id                | Order number                                             |
| Deal_date              | Order date                                               |
| First_deal_date        | Date of first order                                      |
| Secret_dwarf_info_1    | Secret feature by dwarf No. 1                            |
| Secret_dwarf_info_2    | Secret feature by dwarf No. 2                            |
| Secret_dwarf_info_3    | Secret feature by dwarf No. 3                            |
| First_default_date     | First default date                                       |
| Successful_deals_count | How many paid orders were made                           |
| Region                 | Tavern region                                            |
| Tavern                 | Type of tavern                                           |
| Hashed_deal_detail_1   | Classified feature by order No. 1                        |
| Hashed_deal_detail_2   | Classified feature by order No. 2                        |
| Hashed_deal_detail_3   | Classified feature by order No. 3                        |
| Hashed_deal_detail_4   | Classified feature by order No. 4                        |
| Hashed_deal_detail_5   | Classified feature by order No. 5                        |
| Hashed_deal_detail_6   | Classified feature by order No. 6                        |
| Age                    | Age of the gnome who made the order                      |
| Gender                 | The gender of the gnome who made the order               |
| Default                | Did the gnome default on this purchase? 1 - yes, 0 - no. |

## Метрика

ROC-AUC

## Требования

Файл ".csv" с результатом должен содержать колонки «action_id, result» без индекса.
