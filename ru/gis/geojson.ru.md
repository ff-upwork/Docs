{
  "date" : "2019-10-11",
  "keywords" :[ "файл geojson", "что такое файл geojson", "файл", "пример geojson", "расширение файла geojson", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON — формат географических файлов на основе JSON",
  "description":"Узнайте о формате файлов GeoJSON и API, которые могут создавать и открывать файлы GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Что такое файл GeoJSON?

GeoJSON — это формат на основе JSON, предназначенный для представления географических объектов с их непространственными атрибутами. Этот формат определяет различные объекты JSON (нотация объектов JavaScript) и способ их соединения. Формат JSON представляет собой сводную информацию о географических объектах, их пространственных границах и свойствах. Объект этого файла может указывать на геометрию (Point, LineString, Polygon), функцию или набор функций. Объекты отображают адреса и места в виде улиц точек, главных дорог и границ в виде цепочек линий, а также стран, провинций и земельных участков в виде полигонов. Используя GeoJSON, различные мобильные приложения маршрутизации и навигации могут указать зону покрытия своих услуг. Расширением GeoJSON является TopoJSON, который меньше по размеру и кодирует геопространственную топологию.

## Краткая история ##

Инженерная рабочая группа Интернета (IETF) совместно с авторами формата сформировала [РГ GeoJSON](https://datatracker.ietf.org/wg/geojson/charter/) для выпуска GeoJSON в апреле 2015 года. Спецификация GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), новая стандартная спецификация формата GeoJSON, опубликованная в августе 2016 года.

## Формат файла GeoJSON ##

### Координата ###

Координата является основным элементом любых географических данных. Это одно измерение (долгота, широта), представляющее одно число (десятичный формат), а иногда также записывает координату высоты. Время тоже является измерением, но его сложность затрудняет запись его в виде координат. Координаты в обоих JSON и GeoJSON форматируются как числа.

### Должность ###

Упорядоченный массив координат представляет [позицию](https://geojson.org/geojson-spec.html#positions). Это наименьшая единица, которая может обозначать точку на земле.

`[Долгота, широта, высота]`

До выпуска текущей спецификации GeoJSON позволял записывать три координаты на позицию, но новая спецификация этого не позволяет.

### Геометрия ###

Геометрии — это простые формы (точки, кривые и поверхности) в GeoJSON, которые состоят из типа и набора координат. Точка — простейшая геометрическая фигура, представляющая одну позицию.

`{ "тип": "точка", "координаты": [0, 0] }`

### LineStrings ###

По крайней мере, два связанных места используются для представления линии.

`{ "тип": "LineString", "координаты": [[10, 30], [10, 10]] }`

Строки точек и линий — это две простейшие категории геометрии. Оба типа геометрии не затрагивают многих геометрических правил. Точка может быть представлена в любом месте, а линия может иметь более одной точки, даже если точки пересекаются сами с собой.

### Полигоны ###

Геометрия GeoJSON кажется значительно более сложной в полигонах. Многоугольники имеют внутренние и внешние области и могут иметь отверстия внутри.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

По сравнению с LineStrings, в полигонах список координат вложен еще на один уровень и может иметь вырезы наподобие пончиков.

### Уровень координат ###

В формате GeoJSON для свойства координат существует четыре уровня глубины.

### Функции ###

Геометрия является центральной частью GeoJSON, поэтому данные реального мира — это больше, чем эти простые формы, имеющие идентичность и атрибуты. Элементы записывают геометрию, а также их свойства.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

Свойства функции могут быть объектом типа [JSON](http://json.org/), содержащими сопоставления ключевых значений одинарной глубины.

### Коллекция признаков ###

На верхнем уровне файлов GeoJSON FeatureCollection — это наиболее распространенная вещь, которая выглядит так:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

Многие пакеты программного обеспечения для картографии и ГИС поддерживают GeoJSON, включая программное обеспечение GeoDjango, OpenLayers и Geoforge. Он также совместим с PostGIS и Mapnik. Сервисы API карт Google, Yahoo и Bing также поддерживают GeoJSON.

## Использованная литература ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON — Википедия](https://en.wikipedia.org/wiki/GeoJSON)

