# Pentaho Data Integration Community Edition

![](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/master/DE-101%20Modules/Module04/Pentaho/img/Pentaho.png)

[Установка Pentaho](https://www.youtube.com/watch?v=RL-EZCi51gc)

[Pentaho основы](https://www.youtube.com/watch?v=K3X9wIC0jO8)

## 1. Создание JOB и трансформаций в Pentaho с настройкой расписания обновления через планировщик задач в Windows

### Основной JOB
В рамках данного JOBа реализован ETL процесс:
- выгрузка данных из git
- объединение/трансформация

![](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/master/DE-101%20Modules/Module04/Pentaho/img/main1_job.png)

### JOB загрузки данных
Данные загружены двумя разными способами:
- Через шаг Pentaho – "HTTP"
- Через shell скрипт

![](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/master/DE-101%20Modules/Module04/Pentaho/img/job_download_samplestore.png)

### Объединение
В рамках объединения произведено объединение данных с всех листов загруженной на предыдущем шаге книги excel

![](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/master/DE-101%20Modules/Module04/Pentaho/img/transformation_general.png)

### Трансформация
Разобьем данные на разные форматы
- информацию по продуктам сохраним в JSON формате
- информацию о возвратах сохраним в формате XML
- информацию о заказах разобьем по регионам:
    CENTRAL – Одним файлом в формате Excel (xls)
    WEST  -  Несколько  файлов разбитых по штатам в csv
    SOUTH – Один файл формата csv в zip архиве
    EAST – текстовый файл с расширением .dat

![](https://github.com/Artem-ne-Artem/Data-engineering-DL/blob/master/DE-101%20Modules/Module04/Pentaho/img/transformation_for_task.png)

### Запуск JOBа по расписанию
При помощи shell скрипта реализован запуск финального JOBа через модуль Kitchen (PDI) через ```Планировщик задач``` на Windows

```bash
#!/bin/Bash
"C:\Pentaho install\pdi-ce-9.3.0.0-428\data-integration\Kitchen.bat" /file:"D:\YandexDisk\Учеба\13.DE\DataLearn\Module04\Pentaho_introduction\scripts\final_job.kjb" /level:Basic
```
