{
  "date" : "2019-10-11",
  "keywords" :[ "файл qml", "формат файла qml", "что такое файл qml", "файл", "пример qml", "расширение файла qml", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML — формат файла стиля QGIS",
  "description":"Узнайте о формате файлов QML и API, которые могут создавать и открывать файлы QML.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## .QML вариант №

Файл с расширением .qml представляет собой XML-файл, в котором хранится информация о стилях слоев для слоев QGIS. QGIS — это кроссплатформенное ГИС-приложение с открытым исходным кодом, используемое для отображения геопространственных данных с возможностью организации данных в виде слоев. Файлы QML содержат информацию, используемую QGIS для отображения геометрии объектов, включая определения символов, размеры и повороты, маркировку, непрозрачность, режим наложения и многое другое. В отличие от файлов QLR, файлы QML содержат в себе всю информацию о стилях. Файлы QML можно открыть в любом текстовом редакторе, например Notepad++.

## Формат файла QML

QLR, аналогичный [QGS](/ru/gis/qgs/) и [QLR](/ru/gis/qlr/), представляет собой XML-файл, содержащий информацию о стилях для слоев.

На рисунке ниже показаны теги верхнего уровня файла QML (с раскрытыми только renderer_v2 и его тегом символа).

{{< figure src="../qml.png" title="" >}}

## использованная литература

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

