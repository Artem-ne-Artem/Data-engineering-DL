# Модуль 1

## Архитектура аналитического решения

1. `Source Layer` - слой систем источников данных OLTP (Online Transactional Processing) - обработка транзакций;

2. `Storage Layer` - слой хранения данных для аналитики (DW, Data Lake, Data Platform);

3. `Business Layer` - слой доступа к данным для бизнес пользователей через инструменты BI, SQL и т.п. Происходит подключение к системам для просмотра отчётов. 

Иногда используется ещё один слой - `Processing/Compute Layer`, где происходит трансформация данных перед загрузкой в хранилище.

### Вариант архитектуры аналитическго решения компании.
![Architecture](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/main/DE-101%20Modules/Module01/Analytics%20Architecture.png)

## Аналитика в Excel

- Создать дашборд в `Excel` на базе [Sample - Superstore.xls](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/main/DE-101%20Modules/Module01/Sample%20-%20Superstore.xls)

xfun::embed_file(https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/main/DE-101%20Modules/Module01/Dashboard_super_store.pdf)
