{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "розширення", "файл", "формат", "система", "файл TMP", "документи TMP", "файли TMP", "тимчасовий файл", "програма", "програми" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - формат тимчасового файлу",
  "description":"Дізнайтеся про формат файлу TMP та API, які можуть створювати та відкривати файли TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Що таке файл TMP? ##

Файл TMP відноситься до тимчасової резервної копії, сховища або іншої файлової системи, створеної програмою. Час від часу він створюється як невидимий файл і часто знищується під час виходу з програми. Файли TMP також можна використовувати для тимчасового зберігання інформації під час створення нового файлу.

## Формат файлу TMP ##

Файл TMP зазвичай складається з необроблених даних, які використовуються як етап у процесі перетворення матеріалу з одного стилю в інший. Microsoft Word і Apple Safari — це дві програми, які можуть створювати та використовувати формат файлу TMP.

Теоретично створені документи TMP повинні автоматично видалятися, коли програма закривається або машина вимикається. На практиці це не завжди так. У результаті під час навігації документами вашої програми ви можете натрапити на тимчасові файли, які активно не використовуються системою чи іншим програмним забезпеченням.

### Допоміжна пам'ять ###

Віртуальна пам'ять використовується в операційних системах, однак програмам, які використовують величезні обсяги інформації, може знадобитися створювати тимчасові документи.

### Комунікація між процесами ###

Більшість операційних систем надають примітиви для передачі даних між програмами, як-от канали, сокети або основну пам’ять, але найпростішим методом є передача файлів у тимчасовий файл і надання додатку-одержувачу інформації про розташування тимчасового файлу.


## Технічна специфікація ##

Отримання характерних тимчасових імен документів зазвичай забезпечується операційними системами та програмами.
Тимчасові файли можна безпечно генерувати в системах POSIX за допомогою бібліотечних функцій mkstemp або tmpfile. Деякі системи включають попередню програму mktemp POSIX (з тих пір, як її немає). Ці файли зазвичай знаходяться у звичайному тимчасовому каталозі на платформах Unix у /TMP, або %TEMP% (це спеціально для входу) на машинах Windows.

Коли програма зупиняється або документ закривається, тимчасовий файл, створений за допомогою tmpfile, автоматично видаляється. GetTempFileName (Windows) або tmpnam (POSIX) можна використовувати для створення тимчасового імені файлу, яке триватиме довше, ніж програма, яка його створила.

## Посилання ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)