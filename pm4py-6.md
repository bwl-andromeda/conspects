---
создал заметку: 25-06-24
tags:
  - Практика-pm4py
---
# pm4py tutorials - руководство №6 по экспорту данных о событиях

**Введение в экспорт данных о событиях** Это руководство посвящено экспорту данных о событиях с помощью PM4Py и охватывает как простые, так и более сложные задачи. В видео объясняется, как обрабатывать фреймы данных, содержащие данные о событиях, и встроенные объекты событий PM4Py. В нем подчеркивается важность преобразования этих форматов в файлы CSV или XCS для дальнейшего использования.

**Экспорт фреймов данных в виде CSV-файлов** Процесс начинается с импорта CSV-файла в виде фрейма данных pandas, чтобы убедиться, что столбцы имеют правильные имена для совместимости с PM4Py. Использование функции pandas 'to_csv' позволяет легко экспортировать данные обратно в формат CSV, сохраняя при этом стандартные имена столбцов, такие как case_id, ключ действия и временная метка.

**Преобразование между форматами: из фрейма данных в XCS-файл** функция 'write_xes' в PM4Py преобразует фреймы данных непосредственно в файлы XES, сначала преобразуя их во внутренний объект журнала событий, а затем сохраняя его. Аналогичным образом просто сохранить существующий объект журнала событий (например, импортированный из файла XES) обратно в виде другого поддерживаемого типа выходных данных, такого как csv или xcs, с помощью аналогичных шагов преобразования, включающих промежуточные этапы преобразования в рамках платформы pm5