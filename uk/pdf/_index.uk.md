{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "основи" ],
  "description":"Portable Document Format (PDF) — це стандартне представлення документів незалежно від програмного забезпечення, апаратного забезпечення та ОС. Стандарти PDF включають PDF/A, PDF/E, PDF/UA, PDF/VT і PDF/X.",
  "title" :"Формат файлу PDF - Що таке файл PDF?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) — це тип документа, створений Adobe ще в 1990-х роках. Метою цього формату файлів було запровадження стандарту для представлення документів та інших довідкових матеріалів у форматі, незалежному від прикладного програмного забезпечення, апаратного забезпечення, а також операційної системи. Формат файлу PDF має повну можливість містити таку інформацію, як текст, зображення, гіперпосилання, поля форм, мультимедіа, цифрові підписи, вкладення, метадані, геопросторові об’єкти та 3D-об’єкти, які можуть стати частиною вихідного документа.

У більшості випадків наявні документи перетворюються на формат PDF замість створення нового PDF-файлу з нуля. Але це не означає, що немає програмного забезпечення для створення або обробки PDF-файлів.

**(Потрібно поділитися чимось про формат файлу PDF? Ви можете опублікувати свої висновки в розділі [Новини формату файлу PDF](https://news.fileformat.com/t/PDF).)**

## Формат файлу PDF - Коротка історія

Короткий огляд хронології формування PDF-файлу з точки зору хронології такий:

**1993** – Adobe Systems надала специфікації PDF безкоштовно

**2008** - PDF був випущений як відкритий стандарт 1 липня 2008 року та опублікований Міжнародною організацією зі стандартизації як **ISO 32000-1:2008**.

**2008** – Adobe опублікувала публічну патентну ліцензію на безоплатні права у форматі ISO 32000-1 на всі патенти, що належать Adobe, необхідні для створення, використання, продажу та розповсюдження PDF-сумісних реалізацій.

Перша версія PDF, позначена як PDF 1.0, яка пізніше була переглянута до PDF 1.7. PDF 1.7, який став ISO 32000-1, містить деякі нестандартизовані власні технології, а також Adobe XML Forms Architecture (XFA) і розширення JavaScript для Acrobat. 28 липня 2017 року було опубліковано PDF 2.0, відомий як ISO 32000-2:2017, який не містить жодних нестандартизованих технологій.

## Специфікації формату файлу PDF

PDF-файл — це набір байтів, які можна згрупувати в маркери відповідно до правил синтаксису, визначених специфікаціями PDF. Один або більше маркерів об’єднуються, щоб сформувати синтаксичні сутності вищого рівня, переважно об’єкти, які є основними значеннями даних, з яких будується документ PDF.

### Файлова структура PDF-файлів

Вміст PDF-файлу впорядковано всередині файлу в такій послідовності.

|Заголовок
|Тіло
|Таблиця перехресних посилань
|Причіп

#### Заголовок файлу PDF ####

Незалежно від версії PDF, PDF-файл починається із заголовка, що містить унікальний ідентифікатор для PDF і версію формату, як-от %PDF-1.x, де x становить від 1 до 7.

#### Тіло файлу ####

Тіло PDF-файлу складається з послідовності непрямих об’єктів, що представляють вміст документа. Об’єкти, як описано вище, представляють такі компоненти документа, як шрифти, сторінки та зразки зображень. Починаючи з PDF 1.5, тіло також може містити потоки об'єктів, кожен з яких містить послідовність непрямих об'єктів.

#### Таблиця перехресних посилань ####

Таблиця перехресних посилань містить інформацію, яка дозволяє довільний доступ до непрямих об’єктів у файлі, тому не потрібно читати весь файл, щоб знайти певний об’єкт. Таблиця повинна містити однорядковий запис для кожного непрямого об’єкта із зазначенням зсуву в байтах цього об’єкта в тілі файлу. (Починаючи з PDF 1.5, частина або вся інформація про перехресні посилання може альтернативно міститися в потоках перехресних посилань.

#### Трейлер файлу ####

Трейлер PDF-файлу дозволяє читачеві швидко знайти таблицю перехресних посилань і певні спеціальні об’єкти. Читачі, які відповідають вимогам, повинні читати файл PDF з кінця. Останній рядок файлу має містити лише маркер кінця файлу, %%EOF. Два попередні рядки повинні містити, по одному на рядок і в порядку, ключове слово startxref і зміщення байтів у декодованому потоці від початку файлу до початку ключового слова xref в останньому розділі перехресного посилання.

### Об'єкти PDF ###

PDF-файл містить декілька різних типів об’єктів наступних типів

* Логічні значення - представляють умовні істинні або хибні
* Числа - цілі та дійсні значення
* Рядки - містять символи в круглих дужках
* Імена - починаються з символу вперед / наприклад, /ASomewhatLongerName призводить до ASomewhatLongerName
* Масиви – PDF підтримує одновимірні масиви. Масиви вищих розмірів можна створити, використовуючи масиви як вкладені елементи
* Словники - колекція об'єктів у вигляді пар ключ-значення. Він може мати нульові записи.
* Потоки - це послідовність байтів, яка також може мати необмежену довжину
* Null Object - представляє нульове значення

Можуть бути й інші об’єкти, наприклад коментарі, які вводяться знаком % і можуть містити 8-бітові символи.

### Непрямі об'єкти ###

Будь-який об’єкт у файлі PDF можна позначити як непрямий об’єкт. Непрямим об’єктам надається унікальний ідентифікатор об’єкта, за яким інші об’єкти можуть посилатися на нього. Перехресні посилання на них зберігаються в таблиці індексів і позначаються ключовим словом xref, яке слідує за основним текстом і дає зсув у байтах кожного непрямого об’єкта від початку файлу.

### Лінійні та нелінійні макети PDF ###

Макети PDF класифікуються як Lnear і нелінійні залежно від цільових програм та інших факторів.

Нелінійний – нелінійні PDF-файли займають менше місця на диску порівняно з лінійними PDF-файлами. PDF-сторінки документа знаходяться в розкиданому вигляді по PDF-файлу, тому нелінійні файли повільніші порівняно з лінійними.

Лінійний PDF. Лінійні PDF-файли створені таким чином, що вони записуються на диск у лінійному порядку. Для цього не потрібні плагіни браузера, щоб весь документ завантажувався перед показом.

### Огляд об'єктів ###

Як уже згадувалося, тіло PDF – це набір об’єктів, згаданих вище. PDF значною мірою базується на PostScript без функцій керування мовами програмування, як-от команд if і циклу. Команди, видані кодом Postscript для створення графічного вмісту, збираються та позначаються маркерами на додаток до будь-яких файлів, графіки чи шрифтів, на які посилається документ. Весь цей вміст накопичується в одному файлі, у результаті чого виходить скомпонований PostScript.

#### Текст ####

Текст у PDF представлено текстовими елементами, які насправді відображаються гліфами зі шрифтів. Гліф — це графічна форма, яка підлягає всім графічним маніпуляціям, таким як перетворення координат. Через важливість тексту в більшості описів сторінок PDF надає засоби вищого рівня для зручного й ефективного опису, вибору та відтворення гліфів.

#### Графіка ####

Графічні оператори, що використовуються в потоках вмісту PDF, описують зовнішній вигляд сторінок, які мають бути відтворені на пристрої растрового виведення. Засоби призначені як для принтерів, так і для дисплеїв. Графічні оператори утворюють шість основних груп:

* Оператори стану графіки маніпулюють структурою даних, яка називається станом графіки, глобальною структурою, у якій виконуються інші графічні оператори. Стан графіки включає поточну матрицю перетворення (CTM), яка відображає координати простору користувача, що використовуються в потоці вмісту PDF, у координати пристрою виводу. Він також містить поточний колір, поточний контур відсікання та багато інших параметрів, які є неявними операндами операторів малювання.
* Оператори побудови шляху вказують шляхи, які визначають форми, траєкторії ліній і області різного типу. Вони містять оператори для початку нового шляху, додавання до нього відрізків і кривих і закриття.
* Оператори малювання контуру заповнюють контур кольором, малюють обведення вздовж нього або використовують його як межу відсікання.
* Інші оператори малювання малюють певні графічні об’єкти, що описують себе. До них належать зразки зображень, геометрично визначені затінення та цілі потоки вмісту, які, у свою чергу, містять послідовності графічних операторів.
* Текстові оператори вибирають і показують символьні гліфи зі шрифтів (опис гарнітур для представлення текстових символів). Оскільки PDF розглядає гліфи як загальні графічні фігури, багато текстових операторів можна згрупувати з операторами стану графіки або малювання. Однак структури даних і механізми для роботи з описами гліфів і шрифтів є достатньо спеціалізованими.
* Оператори позначеного вмісту пов’язують логічну інформацію вищого рівня з об’єктами в потоці вмісту. Ця інформація не впливає на відтворений вигляд вмісту; це корисно для програм, які використовують PDF для обміну документами.

## Посилання ##

* [Формат файлу PDF: базова структура](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF - Вікіпедія](https://en.wikipedia.org/wiki/PDF)
* [Довідка у форматі PDF – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

