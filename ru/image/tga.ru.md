{
  "date" : "2019-10-11",
  "keywords" :[ "файл tga", "формат файла tga", "что такое файл tga", "файл", "пример tga", "расширение файла tga", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла TGA — файл графического изображения TARGA",
  "description":"Узнайте о формате файла TGA и API-интерфейсах, которые могут создавать и открывать файлы TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .TGA вариант №

Файл с расширением .tga представляет собой растровый графический формат, созданный компанией Truevision Inc. Он был разработан для плат TARGA (Truevision Advanced Raster Adapter) и обеспечивал поддержку отображения Highcolor/truecolor для IBM-совместимых ПК. Он поддерживает 8, 16, 24 и 32 бита на пиксель и 8-битный альфа-канал. Он также поддерживает сжатие RLE без потерь, которое можно применять для уменьшения размера изображения. Цифровые фотографии и текстуры используют формат изображения TGA.

## Краткая история

Формирование формата файла TGA началось в 1984 году компанией AT&T EPICenter (позже извлеченной и сформированной как независимая организация, известная как Truevision), которая работала над маркетингом новых технологий, разработанных AT&T для буферов цветных кадров. EPICenter уже работал над своими первыми двумя картами, VDA (адаптер видеодисплея) и ICB (плата захвата изображения), для которых уже велась работа над двумя типами файлов, .vda и .icb. Эти форматы файлов были кодифицированы, и был введен менее широкий формат файлов TGA. TGA был расширением того, что уже использовалось, и предоставлял такую информацию, как ширина, высота, глубина пикселей, связанная карта цветов и происхождение изображения.

Версия TGA 2.0, опубликованная в 1989 году, включает в себя несколько расширенных функций, таких как:

* Миниатюры
* Альфа-канал
* Значение гаммы
* Текстовые метаданные

Основными участниками версии 2.0 TGA являются Шон Штайнер из Truevision, Кевин Фидли и Дэвид Споэльстра.

## Спецификации формата файла TGA TARGA

Файл TGA состоит из двух основных частей:

* Заголовок
* Информация о цветовом пикселе

Все значения в файле TGA имеют обратный порядок байтов в соответствии со спецификациями формата.

### Заголовок TGA

Заголовок файла TGA состоит из следующих 5 полей.

|Номер поля|Длина |Имя поля |Описание|
---|---|---|---|
|1| 1 байт |длина идентификатора| Длина поля идентификатора изображения (0-255)|
|2| 1 байт |Тип карты цветов| Включена ли карта цветов (0 — указывает, что данные карты цветов не включены в это изображение. 1 — указывает, что карта цветов включена в это изображение.)|
|3| 1 байт |Тип изображения| Типы сжатия и цвета (0 — Данные изображения не включены. 1 — Несжатое, изображение с цветовой картой, 2 — Несжатое, изображение True Color, 9 — Кодированное по длине, изображение с цветовой картой, 11 — Кодированное по длине, черно-белое изображение. )|
|4| 5 байт | Спецификация карты цветов | Описывает цветовую карту|
|5| 10 байт |Спецификация изображения| Размеры и формат изображения|

### Данные изображения и цветовой карты

|Поле нет. |Длина |Поле |Описание|
---|---|---|---|
|6 |Из поля длины идентификатора изображения| Идентификатор изображения | Необязательное поле, содержащее идентифицирующую информацию|
|7 |Из поля спецификации карты цветов| Данные цветной карты| Интерполяционная таблица, содержащая данные цветной карты|
|8 |Из поля спецификации изображения| Данные изображения| Хранится в соответствии с дескриптором изображения|

### Область разработчика (необязательно)

TGA версии 2.0 обеспечивает поддержку дополнительных улучшений/настроек, которые многие разработчики хотели хранить больше информации. Информация необязательна, поэтому, если декодер TGA не сможет ее интерпретировать, она будет проигнорирована.

### Область расширения (необязательно)

|Поле №| Длина| Поле |Описание|
---|---|---|---|
|10| 2 байта |Размер расширения |Размер в байтах области расширения, всегда 495|
|11| 41 байт| Имя автора | Имя автора. Если не используются, байты должны быть установлены в NULL (\0) или пробелы|
|12| 324 байта| Комментарий автора| Комментарий, организованный в виде четырех строк, каждая из которых состоит из 80 символов плюс NULL|
|13| 12 байт| Отметка даты/времени |Дата и время создания образа|
|14| 41 байт| Идентификатор задания||
|15| 6 байт| Время работы| Часы, минуты и секунды, затраченные на создание файла (для выставления счетов и т. д.)|
|16| 41 байт| Идентификатор программного обеспечения | Приложение, создавшее файл. |
|17| 3 байта| Версия ПО||
|18| 4 байта| Ключевой цвет||
|19| 4 байта| Соотношение сторон пикселей||
|20| 4 байта| Гамма-значение||
|21| 4 байта| Смещение цветокоррекции |Число байтов от начала файла до таблицы цветокоррекции, если она есть|
|22| 4 байта| Почтовая марка | Количество байтов от начала файла до изображения почтовой марки, если оно присутствует|
|23| 4 байта| Смещение линии развертки| Количество байтов от начала файла до таблицы строк сканирования, если она присутствует|
|24| 1 байт| Тип атрибута| Определяет альфа-канал|

### Нижний колонтитул файла (необязательно)

Последние 26 байт файла представляют собой нижний колонтитул, который, если он присутствует, означает, что это, скорее всего, файл TGA версии 2.

|Поле №| Длина| Поле| Описание|
---|---|---|---|
|28| 4 байта| Смещение расширения| Смещение в байтах от начала файла|
|29| 4 байта| Смещение области разработчика| Смещение в байтах от начала файла|
|30| 16 байт| Подпись| Содержит "TRUEVISION-XFILE"|
|31| 1 байт| | Содержит "."|
|32| 1 байт| | Содержит NULL |


## использованная литература

* [Спецификации формата файлов TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA из Википедии](https://en.wikipedia.org/wiki/Truevision_TGA)

