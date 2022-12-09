{
  "date" : "2019-10-11",
  "keywords" :[ "файл odp", "формат файла odp", "что такое файл odp", "файл", "пример odp", "расширение файла odp", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP — формат файла презентации OpenOffice",
  "description":"Узнайте о формате файла ODP и API-интерфейсах, которые могут создавать и открывать файлы ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## .ODP вариант №

Файлы с расширением .odp представляют формат файла презентации, используемый OpenOffice.org в стандарте OASISOpen. Файл презентации — это набор слайдов, каждый из которых может содержать текст, изображения, форматирование, анимацию и другие медиафайлы. Эти слайды представляются аудитории в виде слайд-шоу с пользовательскими настройками презентации. Файлы ODP можно открывать приложениями, которые соответствуют формату OpenDocument (например, OpenOffice или StarOffice).

## Краткая история

Спецификации формата файлов ODP основаны на стандарте, разработанном как спецификации ODF. Эти спецификации развивались в прошлом в виде трех версий, разработанных и опубликованных OASIS следующим образом:

`2005` - Версия 1.0 была опубликована в мае 2005 года.
`2007` - Версия 1.1 была опубликована в феврале 2007 года.
`2011` - Версия 1.2 была опубликована в сентябре 2011 года.

При переходе с версии ODF 1.0 на версию 1.1 произошли довольно незначительные изменения. [Версия ODF 1.2] (https://www.oasis-open.org/standards#opendocumentv1.2) является последней версией спецификаций ODF, и разработчики должны консультироваться с ней при разработке приложений, связанных с чтением/записью ODS.

## Спецификации формата файла

Формат OpenDocument поддерживает представление документа в виде одного XML-документа, а также набора нескольких вложенных документов внутри пакета в виде архива [ZIP](https://docs.fileformat.com/Compression/ZIP/). В каждом из файлов ZIP-архива хранится часть полного документа. Каждый вложенный документ хранит определенный аспект документа. Например, один вложенный документ содержит информацию о стиле, а другой вложенный документ содержит содержимое документа. Типичный документ ODF состоит из следующих компонентов:

* `content.xml` – содержимое документа и автоматические стили, используемые в содержании.
* `styles.xml` – стили, используемые в содержимом документа, и автоматические стили, используемые в самих стилях.
* `meta.xml` – метаданные документа, такие как автор или время последнего действия сохранения.
* `settings.xml` – настройки приложения, такие как размер окна или информация о принтере.

Помимо этого, в пакете может быть много других вложенных документов, таких как миниатюры документов, изображения и т. д.

Файлы документов электронных таблиц представляют собой подмножество файлов ODF, в которых содержимое (листы) хранится в поддокументе content.xml.

## использованная литература

* [OpenDocument — Википедия] (https://en.wikipedia.org/wiki/OpenDocument)
