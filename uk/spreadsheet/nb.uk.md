{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "файл", "розширення", "формат файлу", "Mathematica", "Електронна таблиця" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про те, що таке API файлів NB, які можуть створювати та відкривати файли NB.",
  "title" :"NB - формат файлу блокнота Mathematica",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Що таке файл NB?

Файл із розширенням .nb — це формат файлу блокнота Wolfram, який зберігає інструкції для математичних інструкцій у текстовому файлі. Він може містити багато різних типів даних, таких як обчислення в реальному часі, довільні динамічні інтерфейси, повний вхідний текст, введення зображень, автоматичне анотування коду, повний програмний інтерфейс високого рівня та тисячі ретельно організованих функцій і параметрів. Текстові інструкції є вхідними та вихідними даними Mathematica, які генеруються та оновлюються, коли вхідні оператори поміщаються у файл.

## Формат файлу Wolfram Notebook NB – більше інформації

Файли Wolfram Notebook NB зберігаються у звичайному текстовому форматі, який є форматом файлу, який читається людиною. Вміст блокнота впорядковано в розділи як звичайний текст, де кожен представлений групами клітинок, подібно до електронної таблиці. Діапазон цих груп визначається дужкою в кінці кожної клітинки. Стиль, призначений клітинці, визначає її роль у блокноті, як описано нижче.

### Блокноти як мова Wolfram

Якщо планується зберегти Блокнот, що складається з математичних інструкцій для виконання Wolfram Language Kernal, клітинкам у документі автоматично призначається стиль тексту `Input`. Це повідомляє ядру вважати ці інструкції, які виконуються, коли користувач використовує комбінацію клавіш `Shift+Return`. Блокнот Mathematica виглядає так, як показано в наступному прикладі.

{{< figure src="../Wolfram Notebook.jpeg" alt="Формат файлу блокнота Wolfram" >}}

### Блокноти як документи

Блокноти Mathematica можуть бути у форматі документа, щоб побачити те, що ви бачите, те, що ви отримуєте (WYSIWYG). Ці документи є такими ж, як і на екрані чи на друкованому папері, і є інтерактивними. Для цього комірці призначається `Стиль тексту` для відображення вмісту без виконання операторів ядра.

## Експорт блокнотів Mathematica

Блокноти Mathematica можна експортувати у багато різних форматів файлів, таких як PDF, графіка, ГІС, стислі та електронні таблиці.

## Список літератури

* [Основи блокнота Mathematica](https://reference.wolfram.com/language/guide/NotebookBasics.html)

