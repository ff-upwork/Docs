{
  "date" : "2019-10-11",
  "keywords" :[ "файл osm", "что такое файл osm", "файл", "пример osm", "расширение файла osm", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM — формат файла OpenStreetMap",
  "description":"Узнайте о формате файлов OSM и API, которые могут создавать и открывать файлы OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .OSM вариант №

OpenStreetMap (OSM) представляет собой огромную коллекцию добровольно предоставленных хранилищ географической информации в различных типах файлов, использующих различные схемы кодирования для преобразования этих данных в биты и байты. OSM — это совместная работа по созданию бесплатной редактируемой карты мира. Основным результатом этих совместных усилий являются географические данные, а не сама карта. Ограничения на использование или доступность географической информации в большей части мира вызывают необходимость создания OSM. Данные, доступные в OSM, готовы заменить Google Maps для классических приложений (Facebook, Craigslist и т. д.) и данные по умолчанию для приложений GPS-приемника. источники данных.

## Краткая история ##

Вдохновленный успехом Википедии, в 2004 году британский предприниматель Стив Кост создал в Великобритании этот общественный картографический проект. Первоначально он сосредоточился на картографировании Соединенного Королевства. Фонд OpenStreetMap был впервые создан в апреле 2006 года для поддержки развития, расширения и распространения бесплатных геопространственных данных для всех. В декабре 2006 года Yahoo помогла OpenStreetMap сделать аэрофотосъемку для создания карт. Полные данные о дорогах Нидерландов и данные о магистральных дорогах Индии и Китая были предоставлены OSM в апреле 2007 года компанией Automotive Navigation Data (AND). В декабре 2007 года Оксфордский университет стал самой известной организацией, интегрировавшей данные OpenStreetMap на свой основной веб-сайт. С тех пор более 2 миллионов зарегистрированных пользователей вносят данные в этот проект с помощью устройств GPS, аэрофотосъемки и ручных съемок. Эти предоставленные сообществом данные доступны по лицензии Open Database License. Зарегистрированная в Англии некоммерческая организация OpenStreetMap Foundation поддерживала сайт OSM.

## Формат файла OSM ##

Существует множество способов и форматов файлов для хранения географических данных, но формат файла **OSM** ограничен OpenStreetMap. OSM — это специально разработанный стандартный формат, предназначенный для удобной передачи по Интернету. Структурированный упорядоченный формат, закодированный в XML, представляет собой файл .osm. В OpenStreetMap есть четыре опорных элемента для хранения топологической структуры данных:

{{< figure src="../OSM.png" alt="Формат файла OSM" >}}


|Узлы|Пути|Отношения|Теги
---|---|---|---|
|<ul><li> Представляет географическое положение, хранящееся в виде пар широты и долготы.</li><li> Используется для представления объектов карты без размера, таких как горные вершины.</li></ul> |<ul><li> Отсортированные списки узлов, обозначающие полилинию или многоугольник</li><li> Представляйте линейные объекты, такие как дороги и реки, и зоны, такие как парковки, джунгли и парки.</li></ul> |<ul><li> Отсортированные списки узлов и путей представляют их взаимосвязь, как барьеры и развороты на дорогах, автомагистрали охватывают различные существующие пути и области с ямами.</li></ul> |<ul><li> Хранить метаданные об объектах карты.* Всегда привязаны к любому узлу, пути или отношению</li></ul>


Теги используются для характеристики наземных физических объектов (зданий, дорог и т. д.) в OpenStreetMap. Каждый тег связан с географической характеристикой объекта, представленного этим конкретным узлом или отношением. В этой бесплатной системе тегов для описания объекта на карту можно включить неограниченное количество атрибутов. Определенные комбинации ключей и значений, одобренные зарегистрированными пользователями, действуют как неформальные стандарты для часто используемых тегов. Однако новые теги могут быть созданы всякий раз, когда новые аспекты требуют анализа ранее неотображенных атрибутов объектов. Большинство функций используют лишь небольшое количество тегов для описания.

OSM использует три типа файлов для хранения своих основных данных.

OSM обрабатывает все эти файлы с информацией об их деталях форматирования. Но эти файлы создают одни и те же внутренние объекты. Для файлов данных флаг видимости объектов OSM всегда установлен, чего нельзя сказать о файлах истории и изменений.

При обычном использовании существует множество форматов файлов OSM. Форматы файлов определяют кодировку содержимого на диске или в сети в битах и байтах. OSM может читать и записывать максимум из этих форматов.

**XML**

Исходный формат OSM основан на XML. Возвращаемые данные API основной базы данных OSM представлены в формате XML.

**ПБФ**

Шифрование буферов протоколов основано на двоичном формате и является одним из самых компактных форматов.

**O5M/O5C**

Двоичный формат, основанный на более простом формате, но относительно менее используемый. OSM может читать, но не может записывать этот формат.

**OPL**

Простой формат, предлагаемый для использования со стандартными инструментами командной строки UNIX. Близок к CSV-файлам, позволяет размещать одну сущность OSM в одной строке.

**ОТЛАЖИВАТЬ**

Текстовый формат, предназначенный для отладки. OSM может записывать этот формат, но не может читать.

**ЧЕРНАЯ ДЫРА**

Пустой формат, в котором удаляются все данные. OSM может записывать этот формат, но не может читать.

## Хранилище данных OSM ##

В основной базе данных OSM **PostgreSQL** хранится основная копия данных OSM с расширением PostGIS. Для каждого примитива данных основная база данных поддерживает таблицу, в строках которой хранятся отдельные объекты. Все правки обновляют эту базу и все остальные форматы формируются с использованием этой базы. Для переноса данных из одного места в другое создаются многочисленные загружаемые пулы баз данных. Два формата, один с использованием XML, а другой с использованием двоичного формата буфера протокола (PBF), определяют эти пулы. Полные данные хранятся в файле с именем planet.osm.

## Сжатие в файлах OSM ##

Текстовые форматы (XML, OPL и Debug) дополнительно используют сжатие gzip или bzip2.

## Использованная литература ##

* [Руководство по форматам файлов OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Изучите OSM](https://learnosm.org/en/osm-data/getting-data/)

