{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла CPG — файл кодовой страницы ESRI",
  "description":"Узнайте о формате файла CPG и API-интерфейсах, которые могут создавать и открывать файлы CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## .CPG вариант №

Файл CPG — это необязательный файл, для которого требуется шейп-файл ESRI, который используется для указания кодовой страницы для определения используемого набора символов. Они хранятся в формате обычного текстового файла и содержат информацию о кодировке, примененной для создания шейп-файла. Если файл CPG недоступен, шейп-файл использует системную кодировку по умолчанию. Файл CPG, если он присутствует, должен иметь тот же префикс, что и файл [SHP](/ru/gis/shp/), например, roads.shp, roads.cpg.

Файлы CPG можно открывать с помощью ESRI ArcGIS Pro.

### Формат файла CPG — дополнительная информация

При просмотре шейп-файла в ArcCatalog или любом другом приложении ArcGIS вы видите только шейп-файл. Но на самом деле шейп-файл использует другие связанные файлы, которые считываются вместе с основным шейп-файлом. Файл CPG также является одним из них, если он присутствует вместе с основным файлом SHP.

## использованная литература

* [Расширения шейп-файлов
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

