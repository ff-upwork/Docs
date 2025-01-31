{
  "date" : "2019-10-11",
  "keywords" :[ "файл psd", "формат файлу psd", "що таке файл psd", "файл", "приклад psd", "розширення файлу psd", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - формат файлу зображень Photoshop",
  "description":"Дізнайтеся про формат файлу PSD та API, які можуть створювати та відкривати файли PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл PSD?

PSD, Photoshop Document, представляє рідний формат файлу Adobe Photoshop, який використовується для проектування та розробки графіки. Файли PSD можуть містити шари зображень, шари коригування, маски шарів, анотації, інформацію про файли, ключові слова та інші специфічні для Photoshop елементи. Файли Photoshop мають розширення за замовчуванням .PSD і максимальну висоту та ширину 30 000 пікселів, а обмеження довжини – два гігабайти.

## Специфікації формату файлу PSD ##

Дані у файлі PSD зберігаються в порядку байтів старшого байту. Це передбачає заміну коротких і довгих цілих чисел під час читання або запису на платформі Windows. Формат файлу Photoshop ділиться на п'ять основних частин. Він має багато маркерів довжини, які можна використовувати для переходу від однієї секції до іншої. Маркери довжини зазвичай доповнюються байтами для округлення до найближчого 2 або 4-байтового інтервалу. П'ять основних частин:

* Заголовок файлу
* Дані режиму кольору
* Ресурси зображень
* Інформація про шар і маску
* Дані зображення

Для відповідності дані слід записати в усі ці поля розділу, оскільки Photoshop може спробувати прочитати весь розділ. Це також означає, що нулі записуються в пропущені поля під час запису у файл. Поле довжини в розділах, розділених довжиною, слід використовувати, щоб вирішити, коли припинити читання. У більшості випадків поле довжини вказує кількість наступних байтів, а не записів. Під час читання файлу необхідно пам’ятати наступні моменти.

* Значення в стовпці "Довжина" в усіх таблицях наведено в байтах.
* Усі значення, визначені як рядок Unicode, складаються з:
* 4-байтове поле довжини, що представляє кількість символів у рядку (не байтів).
* Рядок значень Unicode, два байти на символ.

### Заголовок файлу ###

Заголовок файлу містить основні властивості зображення.

|Довжина|Опис
---|---|
|4|Підпис: завжди дорівнює '8BPS'. Не намагайтеся прочитати файл, якщо підпис не відповідає цьому значенню.
|2|Версія: завжди дорівнює 1. Не намагайтеся прочитати файл, якщо версія не відповідає цьому значенню. (~*~*PSB~*~* версія 2.)
|6|Зарезервовано: має бути нуль.
|2|Кількість каналів у зображенні, включаючи будь-які альфа-канали. Підтримуваний діапазон від 1 до 56.
|4|Висота зображення в пікселях. Підтримується діапазон від 1 до 30 000.
|4|Ширина зображення в пікселях. Підтримується діапазон від 1 до 30 000.
|2|Глибина: кількість бітів на канал. Підтримувані значення: 1, 8, 16 і 32.
|2|Колірний режим файлу. Підтримувані значення: Bitmap # 0; Відтінки сірого # 1; Індексований # 2; RGB # 3; CMYK # 4; Багатоканальний # 7; Duotone # 8; Лабораторія №9.

### Розділ даних режиму кольору ###

Розділ даних колірного режиму структурований таким чином:


|Довжина|Опис
---|---|
|4|Довжина наступних даних кольору
|змінна|Дані кольору

Дані режиму кольору доступні лише для індексованого кольору та дуотону, як визначено полем режиму в розділі Заголовок файлу. Для всіх інших режимів цей розділ представлено 4-байтовими обнуленими значеннями. Для індексованих кольорових зображень довжина становить 768, а дані про колір містять таблицю кольорів для зображення в порядку без чергування. Для двокольорових зображень дані кольору містять специфікацію двоколірності (формат якої не задокументовано). Інші програми, які читають файли Photoshop, можуть розглядати двоколірне зображення як сіре зображення та просто зберігати вміст двокольорової інформації під час читання та запису файлу.

### Розділ ресурсів зображень ###

Третій розділ файлу містить ресурси зображень. Воно починається з поля довжини, за яким слідує ряд блоків ресурсів.


|Довжина|Опис
---|---|
|4|Довжина розділу ресурсу зображення. Довжина може дорівнювати нулю.
|Змінна|Ресурси зображень (блоки ресурсів зображень)

Ресурси зображень використовуються для зберігання непіксельних даних, пов’язаних із зображеннями, наприклад шляхів інструменту пера. Їх називають блоками ресурсів, оскільки вони містять дані, які зберігалися в ресурсі Macintosh у ранніх версіях Photoshop. Основна структура блоків ресурсів зображень виглядає так:


|Довжина|Опис
---|---|
|4|Підпис: '8BIM'
|2|Унікальний ідентифікатор для ресурсу. Ідентифікатори ресурсів зображень містять список ідентифікаторів ресурсів, які використовуються Photoshop.
|Змінна|Ім'я: рядок Pascal, доповнений, щоб зробити розмір рівномірним (нульове ім'я складається з двох байтів 0)
|4|Фактичний розмір даних ресурсу, що йде далі
|Змінна|Дані ресурсу, описані в розділах про окремі типи ресурсів. Він підбитий, щоб вирівняти розмір.

Ресурси зображень використовують кілька стандартних ідентифікаційних номерів.

### Інформація про шар і маску ###

Четвертий розділ файлу Photoshop містить інформацію про шари та маски, наприклад кількість шарів, канали в шарах, діапазони змішування, ключі коригувального шару, шари ефектів і параметри маски. Якщо немає шарів або масок, цей розділ представлено обнуленим 4-байтовим полем. Особливу увагу при читанні цього розділу необхідно звернути на довжину розділів через нульові значення. Розташування розділу «Шар» і «Маска» таке:


|Довжина|Опис
---|---|
|4|Довжина розділу інформації шару та маски. (Довжина PSB становить 8 байт.)
|Змінна|Інформація про шар
|Змінна|Інформація про глобальну маску шару
|Змінна|Серія блоків із тегами, що містять різні типи даних.

#### Інформація про шар ####

У наступній таблиці показано високорівневу організацію інформації шару.


|Довжина|Опис
---|---|
|4|Довжина інформаційного розділу шарів, округлена до числа, кратного 2. (Довжина PSB становить 8 байтів.)
|2|Кількість шарів. Якщо це від’ємне число, його абсолютне значення є кількістю шарів, а перший альфа-канал містить дані прозорості для об’єднаного результату.
|Змінна|Інформація про кожен шар. У розділі Записи шару описується структура цієї інформації для кожного шару.
|Змінна|Дані зображення каналу. Містить один або кілька записів даних зображення для кожного шару. Шари розташовані в такому самому порядку, як і в інформації про шар

### Дані зображення ###

Піксельні дані зображення містяться в розділі «Дані зображення» файлу. Розташування даних у розділі «Дані зображення» відбувається в планарному порядку, тобто спочатку всі дані червоного кольору, потім усі дані зеленого кольору тощо. Кожна площина зберігається в порядку рядка сканування без байтів. Розділ даних зображення розташовано у форматі як показано в наступній таблиці.

|Довжина|Опис
---|---|
|2|Метод стиснення: *0 = Необроблені дані зображення * 1 = RLE стиснені дані зображення починаються з кількості байтів для всіх рядків сканування (рядки * канали), причому кожна кількість даних зберігається як двобайтове значення. Далі стиснуті дані RLE, кожен рядок сканування стиснутий окремо. Стиснення RLE — це той самий алгоритм стиснення, який використовується програмою Macintosh ROM PackBits і стандартом TIFF. *2 = ZIP без прогнозу *3 = ZIP з прогнозом.
|Змінна|Дані зображення. Планарний порядок = RRR GGG BBB тощо.

## Посилання ##

* [Специфікації формату файлу PSD – від Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Формат файлу Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

