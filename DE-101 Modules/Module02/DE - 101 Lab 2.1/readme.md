# Модуль 2: Базы данных и SQL
## Подключение к Базам Данных и SQL

1. Установка PostgreSQL, Установка клиента SQL для подключения базы данных (DBeaver).
2. Создание 3-х таблиц и загрузка данных из Superstore Excel в БД.
  - [Create table people.sql](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/main/DE-101%20Modules/Module02/DE%20-%20101%20Lab%202.1/people.sql)
  - [Create table returns.sql](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/main/DE-101%20Modules/Module02/DE%20-%20101%20Lab%202.1/returns.sql)
  - [Create table orders.sql](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/main/DE-101%20Modules/Module02/DE%20-%20101%20Lab%202.1/orders.sql)


## Модели Данных

1. Нарисовать модель данных для файлика Superstore
- Концептуальную
- Логическую
- Физическую
  
  [SqlDBM](https://sqldbm.com/Home/)
  
  **Концептуальная модель**
  ![Концептуальная модель](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/main/DE-101%20Modules/Module02/DE%20-%20101%20Lab%202.1/Conceptual_model..png)
  
2. Скопировать DDL и выполнить его в SQL клиенте.
3. Сделать `INSERT INTO SQL`, чтобы заполнить **Dimensions** таблицы и **Sales Fact** таблицу. Сначала мы заполняем **Dimensions** таблицы, где в качестве **id** мы генерим последовательность чисел, а зачем **Sales Fact** таблицу, в которую вставляем **id** из **Dimensions** таблиц. Такой пример я рассматривал в видео.
