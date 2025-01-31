{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу XFDF - що таке файл XFDF?",
  "description":"Дізнайтеся про файл XFDF та API, які можуть створювати та відкривати файли XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл XFDF?

Файл із розширенням .xfdf — це формат даних XML Forms, створений за допомогою програмного забезпечення Adobe Acrobat. Як і [FDF](/uk/pdf/fdf/), XFDF містить опис елементів форми та їхні значення у форматі XML. Це може включати імена та значення текстових полів у формі PDF. XFDF зберігаються у зручному для читання форматі та можуть бути прочитані програмно за допомогою мов програмування, таких як C#.

## Формат файлу XFDF - Додаткова інформація

Файли XFDF зберігаються у форматі файлу XML, який є універсальним форматом, який використовується для імпорту та експорту даних. Структура файлу XFDF складається із заголовка, за яким слідують значення полів і дані елементів, як показано нижче.

|Елемент|Атрибут|Зміст|
---|---|---|
|\<XFDF> ||Найвищий елемент|
|\<fields> ||Усі значення полів для цього шаблону|
|<field (T)> |назва |Назва поля|
|<value (V)> |значення |Значення поля|

## Список літератури

* [Підтримка формату FDF від Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Ресурси для розробників Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

