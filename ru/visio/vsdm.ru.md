{
  "date" : "2019-10-11",
  "keywords" :[ "файл vsdm", "формат файла vsdm", "что такое файл vsdm", "файл", "пример vsdm", "расширение файла vsdm", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM — формат файла чертежа Microsoft Visio",
  "description":"Узнайте о формате файла VSDM и API-интерфейсах, которые могут создавать и открывать файлы VSDM.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
"идентификатор":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## .VSDM вариант №

Файлы с расширением .vsdm — это файлы чертежей, созданные с помощью приложения Microsoft Visio, которое поддерживает макросы. Файлы VSDM представляют собой чертежи OPC/XML, похожие на VSDX, но также обеспечивающие возможность запуска макросов при открытии файла. Макросы — это определяемые пользователем действия/шаги, которые разработаны в Visual Basic для приложений (VBA) и могут использоваться для выполнения повторяющихся задач. Формат файла VSDM был представлен с запуском Microsoft Visio 2013. Файлы Visio используются для создания рисунков, содержащих визуальные объекты, блок-схемы, диаграммы UML, информационные потоки, организационные диаграммы, диаграммы программного обеспечения, макет сети, модели баз данных, сопоставление объектов и другое. аналогичная информация. Файлы, созданные с помощью Visio, также можно экспортировать в файлы различных форматов, таких как [PNG](/ru/image/png/), [BMP](/ru/image/bmp/), [PDF](/ru/pdf/) и другие.

## Формат файла VSDM

Файлы VSDM основаны на соглашениях об открытой упаковке и XML, и разработчики могут извлечь выгоду из этого формата, научившись программно работать с этими файлами. Формат наследует многие из тех же структур XML, что и его части, из формата файла документа Visio XML (.vdx). Совместимость с файлами Visio значительно повышается, поскольку стороннее программное обеспечение может манипулировать файлами Visio на уровне формата файла.

Каждый файл Visio называется пакетом, который содержит другие файлы или части. Часть пакета может быть файлом XML, изображением или даже решением VBA. Части внутри пакета могут быть разделены на части «документ» и «отношения».

### Документ ###

Части документа содержат фактическое содержимое и метаданные файла Visio, такие как имя файла, первая страница и все фигуры, которые она содержит, и даже подключения к данным для фигур. Изображения и текстовые файлы в пакете считаются частями документа.

### Отношения ###

Части отношений файла Visio хранятся в папке «\_rels» и описывают, как части в пакете связаны друг с другом. Он также предоставляет структуру файла. Автономный XML-документ использует отношения родительский/дочерний элементов для определения отношения сущностей друг к другу. Допустимый формат файла Visio 2013 содержит правильный набор частей, а пакет содержит отношения между частями.

Части отношений — это XML-документы, описывающие отношения между различными частями документа в пакете. Они определяют связь между двумя элементами: указанным источником (определяемым именем и расположением файла отношений) и указанной целевой частью документа. Например, части отношений используются для описания того, какие мастера форм связаны с файлом, как страницы связаны с файлом и друг с другом, или как изображения и объекты связаны с определенной страницей.

## Использованная литература ##

* [Введение в формат файла Visio] (https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
