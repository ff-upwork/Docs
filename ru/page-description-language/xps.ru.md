{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Характеристики бумаги XML", "Файл", "Расширение", "Формат файла", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS — формат файла макета страницы",
  "description":"Узнайте о формате файлов XPS и API-интерфейсах, которые могут создавать и открывать файлы XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## .XPS вариант № ##

Файл XPS представляет собой файлы макета страницы, основанные на спецификациях XML Paper, созданных Microsoft. Он был разработан в качестве замены формата файла EMF и подобен формату файла [PDF](/ru/pdf/), но использует XML в макете, внешнем виде и информации для печати документа. На самом деле более оправданно будет сказать, что XPS является попыткой PDF, но не может получить достаточную популярность, поскольку принадлежит PDF по многим причинам. Microsoft предоставляет XPS Document Writer по умолчанию, начиная с Windows 7, для создания файлов XPS. Файлы XPS можно создать, выбрав «Microsoft XPS Document Writer» в качестве принтера при печати документа.

Средства просмотра XPS интегрированы в Windows Vista, Windows 7, Windows 8 и Internet Explorer 6 или более поздней версии. Файлы XPS становятся доступными только для чтения после их создания. Это повышает уверенность пользователя в подлинности полученных документов, отправленных в формате XPS. Документ XPS может содержать одну или несколько страниц, преобразованных из исходного документа.

## Краткая история ##

Microsoft представила спецификацию XPS в Ecma International. В июне 2007 года был создан Технический комитет 46 Ecma (TC46) для разработки стандарта на основе спецификаций OpenXPS Paper. Ecma International утвердила стандарт Ecma (ECMA-388) [спецификации XPS] (http://www.ecma-international.org/publications/standards/Ecma-388.htm) в июне 2009 г. на 97-й Генеральной Ассамблее.

## Формат файла XPS ##

Формат XPS состоит из разметки XML, которая определяет состав документа и внешний вид каждой страницы, а также правила рендеринга для отображения или печати документа. Он сохраняет всю информацию для повторного создания документа в любой системе, что делает его независимым от ресурсов, доступных в этой системе. По сути, это ZIP-архив, и если вы переименуете расширение файла в ZIP, вы увидите составляющие файлы, содержащие данные документа. Эти документы включают в себя:

* файлы страниц документа (.fpage) — содержит содержимое документа и настройки формата документа. Каждая страница в документе XPS имеет один файл FPAGE.
* файл настроек документа (.fdoc) — хранит настройки, включенные в архив XPS.
* файлы фрагментов документа (.frag) — определяет параметры для фактического файла XPS, и каждая страница в документе имеет свой собственный файл .frag.

{{< figure src="../XPS-1.png" alt="Формат файла XPS" >}}

Эти файлы сохраняют содержимое документа таким образом, что если, например, у кого-то не установлены те же шрифты на его компьютере, средство просмотра XPS по-прежнему будет отображать эти исходные шрифты. Это подразумевает включение файла разметки XML для каждого:

* Страница
* Текст
* Встроенные шрифты
* Растровые изображения
* 2D векторная графика
* Управление цифровыми правами

Формат документа XPS включает четко определенный набор частей и взаимосвязей, каждая из которых служит определенной цели в документе. Формат также расширяет возможности пакета, включая цифровые подписи, эскизы и чередование.

Типичный XPS-документ выглядит следующим образом и может быть проанализирован в свете формата файлов XPS [спецификаций] (https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="Формат файла XPS" >}}


## Использованная литература ##

* [Спецификации формата файлов XPS](http://www.ecma-international.org/publications/standards/Ecma-388.htm)
* [XPS — Википедия] (https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)
