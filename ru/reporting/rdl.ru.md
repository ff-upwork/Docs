{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL — файл определения отчета на языке",
  "keywords" :[ "rdl", "язык определения отчета", "XmlTextWriter", "XSD", "элемент RDL"],
  "description":"Узнайте о формате файла RDL, который представляет собой XML-представление определения отчета служб SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## .RDL вариант № ##

RDL (язык определения отчетов) — это эталон, установленный Microsoft для определения отчетов. Файл RDL состоит из одного или нескольких элементов RDL. Принимая во внимание, что элемент RDL состоит из его типа данных и количества элементов. Элемент может быть простым или сложным. У простого элемента нет дочерних элементов или атрибутов, тогда как у сложного элемента есть дочерние элементы и необязательные атрибуты.

## Определение XML-схемы RDL
Файл определения схемы XML (XSD) проверяет файл RDL. Схема определяет правила размещения элементов RDL в файле .rdl. Элемент RDL может быть простым или сложным. У простого элемента нет дочерних элементов или атрибутов, а у сложного элемента есть дочерние элементы и, возможно, атрибуты.

## Создание RDL
Поскольку RDL является открытым и расширяемым по своей природе, многие приложения и инструменты могут быть созданы для создания RDL-файлов на основе его XML-схемы. Один из самых простых способов создать RDL из приложения — использовать классы Microsoft .NET Framework пространства имен **System.Xml** и пространства имен System.Linq. В частности, класс **XmlTextWriter** можно использовать для написания RDL. Вы можете сгенерировать полное определение отчета от начала до конца в любом приложении .NET Framework с помощью **XmlTextWriter**. Разработчики также могут добавлять настраиваемые элементы отчета с настраиваемыми свойствами для расширения RDL.

## Типы RDL
В следующей таблице перечислены типы и атрибуты, используемые в элементах RDL.

|Тип|Описание|
---|---|
|Двоичный |Свойство с двоичным значением в кодировке Base-64.|
|логическое значение| Свойство со значением true или false в качестве значения объекта. Если не указано иное, значение пропущенного необязательного логического объекта равно False.|
|Дата |Свойство с полностью указанной датой или значением даты и времени, указанным в формате даты ISO8601: ГГГГ-ММ-ДД[ЧЧ:ММ[:СС[.С]]].|
|Enum |Свойство со строковым текстовым значением, которое должно быть одним из списка назначенных значений.|
|Float |Свойство со значением с плавающей запятой. Точка (.) используется как необязательный десятичный разделитель.|
|Integer |Свойство с целочисленным значением (int32).|
|Language |Свойство с текстовым значением, которое содержит код языка и региональных параметров, например "en-us" для американского английского. Значение должно быть либо конкретным языком, либо нейтральным языком, для которого в Microsoft .NET Framework определен язык по умолчанию.|
|Имя |Свойство со строковым текстовым значением. Имена должны быть уникальными в пределах пространства имен элемента. Если не указано иное, пространством имен для элемента является самый внутренний содержащий объект, имеющий имя.|
|NormalizedString |Свойство с текстовым строковым значением, которое было нормализовано.|
|Размер |Элемент размера должен содержать число (с символом точки, используемым в качестве необязательного десятичного разделителя). За числом должно следовать обозначение единицы длины CSS, например см, мм, дюйм, пункт или ПК. Пробел между номером и обозначением необязателен. Дополнительные сведения об обозначениях размеров см. в разделе Справочник по значениям и единицам измерения CSS. В RDL максимальное значение параметра «Размер» — 160 дюймов. Минимальный размер — 0 дюймов.|
|String |Свойство со строковым текстовым значением.|
|UnsignedInt |Свойство со значением целого числа без знака (uint32).|
|Вариант |Свойство с любым простым XML-типом.|

## Типы данных RDL
В RDL перечисление DataType определяет тип данных атрибута, выражения или параметра. В следующей таблице показано, как типы данных CLR соответствуют типам данных RDL.

|Типы CLR |Соответствующий тип данных|
---|---|
|логическое значение| логический |
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Одинарный, двойной |Плавающий|
|Строка, Символ, GUID, Промежуток времени |Строка|


## Использованная литература ##

- [Язык определения отчета (Википедия)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Язык определения отчетов (SSRS)] (https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)
