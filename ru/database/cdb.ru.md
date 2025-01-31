{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "расширение", "файл cdb", "формат файла cdb", "Тип файла базы данных", "Формат файла базы данных", "что такое файл cdb"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файлов CDB и API, которые могут создавать и открывать файлы CDB.",
  "title" :"CDB - Постоянный файл базы данных",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## .CDB вариант №
Файлы CDB используются в критически важных приложениях, таких как электронная почта. CDB расшифровывается как «база данных констант», быстрый, надежный и простой пакет для создания или чтения баз данных констант. Замена базы данных защищена от сбоев системы. Пользователям не нужно делать паузу во время перезаписи. CDB работает как ассоциативный массив (на диске), сопоставляя ключи со значениями и позволяя хранить несколько значений в одном ключе.

## Формат файла CDB
Формат файла CDB хранит числа, смещения, длины и хэш-значения в формате с прямым порядком байтов как 32-разрядные целые числа без знака. Ключи и данные считаются непрозрачными строками байтов без специальной обработки. В начале базы данных заголовок фиксированного размера представляет 256 хэш-таблиц, перечисляя их положение в файле и их длину в слотах. Обычно данные хранятся в виде последовательности записей, каждая запись хранит длину ключа, длину данных, ключ и данные. Нет правил сортировки или выравнивания. За записями следует набор из 256 хэш-таблиц различной длины. Поскольку допустимой длиной является ноль, в базе данных может быть физически сохранено менее 256 хеш-таблиц, но ничто не считается 256 таблицами. Хэш-таблицы состоят из ряда слотов, каждый из которых содержит хеш-значение и смещение записи. «Пустые слоты» имеют нулевое смещение.

### Структура
База данных CDB состоит из всего набора данных в одном компьютерном файле. Он состоит из трех частей:
- Заголовок фиксированного размера
- Данные
- Набор хеш-таблиц.

Поиск доступен только для точных ключей. Поиски действуют по следующему алгоритму:

- Хэш ключ.
- Определите, в какой хеш-таблице и слоте должна находиться эта запись.
- Протестировать указанный слот в хеш-таблице.

Для поиска ключей с более чем одним значением можно найти дополнительные значения, просто возобновив поиск в следующем слоте.

#### Функции

Структура базы данных CDB обеспечивает несколько функций:

##### Быстрый поиск
Успешный поиск в огромной базе данных обычно занимает всего два обращения к диску, а неудачный поиск — только один.
##### Низкие накладные расходы
База данных использует 2048 байтов, 24 байта на запись и пространство для ключей и данных.
##### Нет случайных ограничений
CDB может управлять любой базой данных размером до 4 гигабайт. Поскольку других ограничений нет, записи даже не должны помещаться в память. Базы данных хранятся в машинно-независимом формате.
##### Быстрая атомарная замена базы данных
Команда **cdbmake** может перезаписать всю базу данных на два порядка быстрее, чем другие пакеты хеширования.
##### Быстрые дампы базы данных
**cdbdump** может распечатать содержимое базы данных в формате, совместимом с cdbmake.


## Использованная литература ##

* [cdb (программное обеспечение) - Википедия](https://en.wikipedia.org/wiki/Cdb_(software))
* [Спецификация CDB](http://cr.yp.to/cdb.html)

