{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Встроенный язык Maya", "файл", "расширение", "формат файла", "Maya 3D", "Руководство по программированию" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL — формат файла встроенного языка Maya",
  "description":"Узнайте о формате файла MEL и API-интерфейсах, которые могут создавать и открывать файлы MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## .MEL вариант №

Файл с расширением .mel (Maya Embedded Language) — это язык сценариев, используемый Autodesk Maya для создания графических интерфейсов. Он позволяет автоматизировать создание графических элементов с помощью исполняемых скриптов в дополнение к графическому интерфейсу Maya. MEL позволяет создавать графические интерфейсы без изучения программирования. Это достигается за счет создания макросов и настраиваемых действий, которые ускоряют выполнение повторяющихся задач. Эти процедуры и сценарии позволяют создавать собственные модели, анимации, динамику и рендеринг задач. Autodesk Maya 2020 можно использовать для открытия и просмотра содержимого файла EML.

## Формат файла MEL — дополнительная информация

[Справочное руководство](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) программиста доступно для разработчиков в разделе документации Maya. MEL основан на командах сценариев оболочки, подобных UINX, для достижения целей. Команды, основанные на сценариях, делают его нерелевантным для обычного и объектно-ориентированного программирования (ООП), что приводит к отсутствию использования структур данных, вызова функций или использования ООП, как в других языках.

Вот некоторые ключевые моменты, касающиеся MEL.

`Комментарии`. Каждое выражение в MEL должно заканчиваться точкой с запятой (;), даже в конце блока.

`Возвращаемые значения`. Указание выражения, возвращающего значение, не приводит к автоматической печати значения в MEL. Вместо этого это вызывает ошибку.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
«Команды для создания, редактирования и удаления». Одна и та же команда используется для создания вещей, редактирования вещей или запроса информации о существующих вещах. Однако флаг определяет, что (создание, редактирование или запрос) делает команда.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
«Возврат значения из функции» — синтаксис функции автоматически возвращает значение. Чтобы получить возвращаемое значение с использованием синтаксиса команды, вы должны заключить команду в обратные кавычки.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## использованная литература

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

