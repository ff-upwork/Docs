{
  "date" : "2019-12-09",
  "keywords" :[ "файл zip", "формат файлу zip", "що таке файл zip", "файл", "приклад zip", "розширення файлу zip", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIP",
  "description":"Що таке файл ZIP і API, які можуть створювати та відкривати файли ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Що таке файл ZIP? ##

Файл із розширенням .zip — це архів, який може містити один або декілька файлів або каталогів. Архів може бути стиснутий до включених файлів, щоб зменшити розмір ZIP-файлу. Формат файлу ZIP був опублікований ще в лютому 1989 року Філом Кацом для досягнення архівації файлів і папок. Формат став частиною утиліти [PKZIP](https://www.pkware.com/pkzip), створеної компанією PKWARE, Inc. Одразу після появи [доступних специфікацій](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), багато компаній зробили формат файлу ZIP частиною своїх програмних утиліт, зокрема Microsoft (починаючи з Windows 7), Apple (Mac OS X) та багато інших.

## Коротка історія формату ZIP

Історія формату файлу ZIP бере свій початок із судового позову, поданого System Enhancement Associates (SEA) проти PKWARE за використання його утиліти ARC без дозволу на його товарний знак і авторські права на зовнішній вигляд продукту та інтерфейс користувача. До цього Філ Кац переписав вихідний код SEA і випустив PKXARC, засіб витягування ARC, і PKARC, компресор файлів, як безкоштовні програми для систем на базі MS-DOS. Програвши судовий процес, PKWARE більше не могла використовувати нічого, пов’язане з ARC. Саме тут виникло створення нового стиснення файлів, названого ZIP, яке було зроблено частиною утиліти PKZIP у PKWARE, Inc.

Катц оприлюднив специфікації формату файлу ZIP у загальному доступі, зберігаючи при цьому права власності на свою утиліту стиснення та вилучення, тобто PKZIP. Система стиснення ZIP могла (і може) архівувати файли в папці за допомогою 32-розрядного алгоритму циклічної перевірки надмірності ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) для стиснення файлу розміри. На відміну від ARC, папки .ZIP включали файл каталогу, який відігравав роль кодової книги криптографа, зберігаючи інформацію, необхідну для відтворення стиснутих файлів.

## Підтримувані методи стиснення в ZIP

Відповідно до специфікацій формату файлу .ZIP підтримуються такі методи стиснення.

* Store - передбачає відсутність стиснення
* Зменшення
* Зменшення (це передбачає коефіцієнти стиснення від рівня 1 до рівня 4)
* Вибухнути
* Здути
* Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd версія I, ред. 1

DEFLATE — це широко використовуваний метод стиснення, який є алгоритмом стиснення дати без втрат, який використовує комбінацію кодування LZ77 і Хаффмана та детально описаний у [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Специфікації формату файлу ZIP

ZIP-файли мають можливість зберігати кілька файлів з використанням різних методів стиснення, і в той же час підтримують збереження файлу без будь-якого стиснення. Кожен файл зберігається/стиснеться окремо, що допомагає розпакувати їх або додати нові без застосування стиснення чи розпакування всього архіву.

### Загальний формат файлу ZIP

Кожен Zip-файл структуровано таким чином:


|Формат файлу ZIP
---|
|Заголовок локального файлу 1
|Дані файлу 1
|Дескриптор даних 1
|Заголовок локального файлу 2
|Дані файлу 2
|Дескриптор даних 2
| ....
| ....
|Заголовок локального файлу N
|Дані файлу N
|Дескриптор даних N
|Заголовок розшифровки архіву
|Архівувати додаткові дані
|Центральний каталог

Формат файлу ZIP використовує 32-розрядний алгоритм CRC для цілей архівування. Щоб відтворити стислі файли, ZIP-архів містить каталог у кінці, який зберігає записи про файли та їх розташування в архівному файлі. Таким чином, він відіграє роль кодування для інкапсуляції інформації, необхідної для відтворення стиснених файлів. Програми читання ZIP використовують каталог для завантаження списку файлів без читання всього архіву ZIP. Формат зберігає подвійні копії структури каталогу, щоб забезпечити кращий захист від втрати даних.

Кожен файл у ZIP-архіві представлено як окремий запис, де кожен запис складається із заголовка локального файлу, за яким слідують дані стисненого файлу. Каталог у кінці архіву містить посилання на всі ці записи файлів. Програми для читання ZIP-файлів повинні уникати читання заголовків локальних файлів, а всі види списків файлів слід читати з каталогу. Цей каталог є єдиним джерелом дійсних записів файлів в архіві, оскільки файли також можна додавати в кінець архіву. Ось чому, якщо читач читає локальні заголовки ZIP-архіву з самого початку, він може прочитати недійсні (видалені) записи, а також ті, що не є частиною каталогу, який видаляється з архіву.

Порядок записів файлів у центральному каталозі не повинен збігатися з порядком записів файлів в архіві.

### Записи файлів ZIP

Записи в ZIP-файлі розташовані один за одним, де кожен запис складається з:

* Заголовок локального файлу
* Додаткові поля даних
* Дані користувача (опціонально стиснуті/опціонально зашифровані)

Заголовок локального файлу кожного запису представляє інформацію про файл, таку як коментар, розмір файлу та ім’я файлу. Додаткові поля даних (необов’язкові) можуть містити інформацію про параметри розширення формату ZIP.

#### Заголовок локального файлу

Заголовок локального файлу має певну структуру поля, що складається з багатобайтових значень. Усі значення зберігаються в порядку байтів у порядку байтів, де довжина поля розраховує довжину в байтах. Усі структури в ZIP-файлі використовують 4-байтові підписи для кожного запису файлу. Підпис кінця центрального каталогу — 0x06054b50, і його можна розрізнити за допомогою власного унікального підпису. Далі наведено порядок інформації, що зберігається в заголовку локального файлу.


|Зсув|Байт|Опис
---|---|---|
|0|4|Підпис заголовка локального файлу # 0x04034b50 (читається як число від порядкового порядку)
|4|2|Версія, необхідна для вилучення (мінімум)
|6|2|Бітовий прапор загального призначення
|8|2|Метод стиснення
|10|2|Час останньої зміни файлу
|12|2|Дата останньої зміни файлу
|14|4|CRC-32
|18|4|Стиснутий розмір
|22|4|Нестиснутий розмір
|26|2|Довжина імені файлу (n)
|28|2|Довжина додаткового поля (м)
|30|n|Назва файлу
|30+n|m|Додаткове поле

#### Заголовок файлу центрального каталогу


|Зсув|Байт|Опис
---|---|---|
|0|4|Підпис заголовка файлу центрального каталогу # 0x02014b50
|4|2|Версія створена
|6|2|Версія, необхідна для вилучення (мінімум)
|8|2|Бітовий прапор загального призначення
|10|2|Метод стиснення
|12|2|Час останньої зміни файлу
|14|2|Дата останньої зміни файлу
|16|4|CRC-32
|20|4|Стиснутий розмір
|24|4|Нестиснутий розмір
|28|2|Довжина імені файлу (n)
|30|2|Довжина додаткового поля (м)
|32|2|Довжина коментаря файлу (k)
|34|2|Номер диска, де починається файл
|36|2|Атрибути внутрішнього файлу
|38|4|Атрибути зовнішнього файлу
|42|4|Відносне зміщення заголовка локального файлу. Це кількість байтів між початком першого диска, на якому знаходиться файл, і початком заголовка локального файлу. Це дозволяє програмному забезпеченню читати центральний каталог, щоб визначити місце розташування файлу в ZIP-файлі.
|46|n|Ім'я файлу
|46+n|m|Додаткове поле
|46+n+m|k|Коментар файлу

#### Кінець запису центрального каталогу


|Зсув|Байт|Опис
---|---|---|
|0|4|Кінець підпису центрального каталогу # 0x06054b50
|4|2|Номер цього диска
|6|2|Диск, де починається центральний каталог
|8|2|Кількість записів центрального каталогу на цьому диску
|10|2|Загальна кількість записів центрального довідника
|12|4|Розмір центрального каталогу (байти)
|16|4|Зсув початку центрального каталогу відносно початку архіву
|20|2|Довжина коментаря (n)
|22|n|Коментар

## Список літератури

* [Специфікації формату ZIP-файлу PKWARE](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Структура файлу PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)
