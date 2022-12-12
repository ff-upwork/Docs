{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml", "файл jhtml", "формат файлу jhtml", "тип файлу jhtml", "файл", "тип", "що таке файл jhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - файл Java HTML",
  "description":"Дізнайтеся про формат файлів JHTML та API, які можуть створювати та відкривати файли JHTML.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## Що таке файл JHTML?

Файл із розширенням .jhtml — це файл [HTML](/uk/web/html/) із кодом [Java](/uk/programming/java/), який виконується на сервері, коли клієнт запитує цю сторінку у браузері. Сервер обробляє запити, виконує функції Java, що містяться у функції, і повертає сторінку в браузер клієнта. Об’єкти Java, вбудовані в сторінки JHTML, запускаються на сервері для обробки запитів на сторінки цього типу. Файли JHTML також можуть отримувати доступ до інформації з бази даних за допомогою підключення JDBC (Java [Database](/uk/database/) Connectivity). Файли JHTML можна відкривати в будь-якому текстовому редакторі та переглядати у таких веб-браузерах, як Google Chrome, Firefox і Safari.

## Формат файлу JHTML

JHTML є власною технологією ATG і може бути створений за допомогою редактора документів Dynamo ATG (Art Technology Group). Файли JHTML записуються у форматі простого тексту за допомогою стандартного коду HTML і Java. Вони містять стандартні теги HTML на додаток до власних тегів, які посилаються на об’єкти Java. Коли користувач запитує таку сторінку, HTTP-сервер пересилає запит на сервер додатків Java. Сторінка JHTML спочатку перетворюється на файл .java і компілюється для створення файлу [.class](/uk/programming/class/), який виконується як сервлет. Це генерує потік стандартних даних HTTP і HTML, які повертаються назад до запитуючого браузера для відображення користувачеві. Це корисно для виконання запитів, пов’язаних із базою даних, на сервері та повернення остаточного накопиченого результату в браузер клієнта.

## Список літератури

* [Глобальна структура документа HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)
