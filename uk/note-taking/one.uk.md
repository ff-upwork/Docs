{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - формат файлу Microsoft OneNote",
  "description":"Дізнайтеся про ОДИН формат файлу та API, які можуть створювати та відкривати ОДИН файл.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл .ONE? ##

Файл із розширенням .ONE створюється програмою Microsoft OneNote. OneNote дозволяє збирати інформацію за допомогою програми так, ніби ви використовуєте чернетковий блокнот для нотаток. Файли OneNote можуть містити різні елементи, які можна розміщувати у нефіксованих місцях на сторінках документа. Ці елементи можуть містити текст, оцифрований рукописний текст і об’єкти, скопійовані з інших програм, включаючи зображення, малюнки та мультимедійні (аудіо/відео) кліпи. Тепер Microsoft пропонує онлайн-версію OneNote як частину Office365, де можна ділитися нотатками з іншими користувачами OneNote через Інтернет.

## Специфікації формату файлу .ONE ##

Формат файлу OneNote забезпечує ефективний спосіб представлення цифрових нотаток у вигляді ієрархічних наборів розділів і сторінок. Кожна сторінка містить визначений користувачем вміст у певній структурі для представлення у форматі файлу Document Object Model (DOM). Модель даних для цього формату показана нижче.

### Огляд структури ###

Як показано в моделі даних для формату файлу OneNote, документ OneNote складається з різних елементів.

#### Розділ ####

Розділ — це найвищий контейнер у файлі OneNote, який містить різні елементи, наприклад:

* Сторінки
* Метадані
* Властивості

Метадані та властивості включають назву розділу, ідентифікацію сторінок, які містяться в розділі, і порядок, у якому ці сторінки відображаються. Термін «розділ» стосується всіх сторінок у розділі та представлення цих даних у файлі сховища версій OneNote®, який має розширення імені файлу .one.

#### Сторінка ####

Визначений користувачем вміст у документі OneNote міститься всередині сторінки. Інформація про сторінку включає текст, списки, таблиці, заголовки сторінок, зображення та теги приміток. Сторінка складається з структурних об’єктів, до яких додається більшість наявних об’єктів. Кожній сторінці можна призначити ім’я для значущого представлення, а об’єкти також можна додавати безпосередньо до сторінок. Сторінка може додатково містити підсторінки в ієрархічній системі.

#### Властивості та набори властивостей ####

Вміст OneNote складається з властивостей, наборів властивостей і об’єктів даних файлів. Набір властивостей — це набір властивостей, який представляє певний тип вмісту. Об’єкт даних файлу – це блок двійкових даних, який містить зображення, вбудовані файли або аудіо/відеовміст.

#### Блокнот OneNote ####

Блокнот — це набір файлів розділів, які зберігаються в одному каталозі. Набір властивостей використовується для визначення таких параметрів, як порядок розділів у блокноті та колір блокнота.

### Структура файлу ###

Файл сховища версій ПОВИНЕН починатися зі структури **Заголовка**. Залишок файлу розділено на блоки байтів, де розмір і структура кожного блоку вказуються полем, яке посилається на нього. Блок доступний, якщо на нього посилається структура **Header** або якщо на нього посилається поле в іншому доступному блоці. Дані поза структурою **Header** і будь-які доступні блоки ПОВИННІ ігноруватися.

Усі структури вирівнюються на межі 1 байт. Усі цілі числа мають знак, якщо не вказано інше. Усі поля мають формат [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), якщо не вказано інше.

#### Заголовок ####

Заголовок файлу .ONE складається з фрагментів, які містять різні унікальні ідентифікатори та поля для представлення інформації про файл, як показано нижче:

`guidFileType (16 байтів):` GUID, який визначає тип файлу сховища версій. ПОВИННО бути одним із значень із наведеної нижче таблиці.


|Формат файлу|Значення
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 байт):` GUID, який визначає ідентичність цього файлу сховища версій. ПОВИНЕН бути унікальним у всьому світі.

`guidLegacyFileVersion (16 байтів):` ПОВИНЕН бути "{00000000-0000-0000-0000-000000000000}" і ПОВИНЕН ігноруватися.

`guidFileFormat (16 байтів):` GUID, який вказує, що файл є файлом сховища версій. МАЄ бути "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 байти):` Ціле число без знаку. ПОВИННО бути одним із значень у наведеній нижче таблиці залежно від типу файлу.

|Формат файлу|Значення
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 байти):` Ціле число без знаку. ПОВИННО бути одним із значень у наведеній нижче таблиці залежно від формату цього файлу.


|Формат файлу|Значення
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 байти):` Ціле число без знаку. ПОВИННО бути одним із значень у наведеній нижче таблиці залежно від формату цього файлу.

|Формат файлу|Значення
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 байти):` Ціле число без знаку. ПОВИННО бути одним із значень у наведеній нижче таблиці, залежно від формату цього файлу.

|Формат файлу|Значення
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 байтів):` структура **FileChunkReference32**, яка ПОВИННА мати значення «fcrZero».

`fcrLegacyTransactionLog (8 байтів):` Структура **FileChunkReference32**, яка ПОВИННА бути "fcrNil".

`cTransactionsInLog (4 байти):` Ціле число без знаку, яке визначає кількість транзакцій у журналі транзакцій. НЕ ПОВИННО дорівнювати нулю.

`cbLegacyExpectedFileLength (4 байти):` Ціле число без знаку, яке ПОВИННО дорівнювати нулю та ПОВИННО ігноруватися.

`rgbPlaceholder (8 байтів):` Ціле число без знаку, яке ПОВИННО бути нулем і ПОВИННО ігноруватися.

`fcrLegacyFileNodeListRoot (8 байтів):` Структура **FileChunkReference32**, яка ПОВИННА бути "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 байти):` Ціле число без знаку, яке ПОВИННО бути нулем і ПОВИННО ігноруватися.

`fNeedsDefrag (1 байт):` НЕОБХІДНО ігнорувати.

`fRepairedFile (1 байт):` НЕОБХІДНО ігнорувати.

`fNeedsGarbageCollect (1 байт):` НЕОБХІДНО ігнорувати.

`fHasNoEmbeddedFileObjects (1 байт):` Ціле число без знаку, яке ПОВИННО бути нулем і ПОВИННО ігноруватися.

`guidAncestor (16 байтів):` Ідентифікатор GUID, який визначає поле **Header.guidFile** файлу змісту, наданого такою таблицею:


|Формат файлу змісту|Розташування файлу змісту
--- | --- |
|Файл розділу - .One|Файл змісту знаходиться в тому ж каталозі, що й цей файл.
|Файл змісту - .onetoc2|Файл змісту знаходиться в батьківському каталозі цього файлу.

Якщо GUID — {00000000-0000-0000-0000-000000000000}, це поле не посилається на файл змісту.

`crcName (4 байти):` Ціле число без знаку, яке визначає значення CRC назви цього файлу сховища версій. Ім’я — це представлення імені файлу в кодуванні Unicode із його розширенням і додатковим нульовим символом у кінці. Цей CRC завжди обчислюється за допомогою алгоритму CRC для файлу .one, незалежно від цього формату файлу сховища версій.

`fcrHashedChunkList (12 байтів):` структура **FileChunkReference64x32**, яка вказує посилання на перший **FileNodeListFragment** у хешованому списку фрагментів. Якщо значення структури **FileChunkReference64x32** є "fcrZero" або "fcrNil", хешований список фрагментів не існує.

`fcrTransactionLog (12 байтів):` структура **FileChunkReference64x32**, яка вказує посилання на першу структуру **TransactionLogFragment** у журналі транзакцій. Значення поля **fcrTransactionLog** НЕ ПОВИННО бути "fcrZero" і НЕ ПОВИННО бути "fcrNil".

`fcrFileNodeListRoot (12 байтів):` Структура **FileChunkReference64x32**, яка вказує посилання на список вузлів кореневого файлу. Значення поля **fcrFileNodeListRoot** НЕ ПОВИННО бути "fcrZero" і НЕ ПОВИННО бути "fcrNil".

`fcrFreeChunkList (12 байтів):` структура **FileChunkReference64x32**, яка вказує посилання на першу структуру **FreeChunkListFragment**. Якщо значення структури **FileChunkReference64x32** є "fcrZero" або "fcrNil", то список вільних блоків не існує.

`cbExpectedFileLength (8 байтів):` Ціле число без знаку, яке визначає розмір у байтах цього файлу сховища версій.

`cbFreeSpaceInFreeChunkList (8 байтів):` Ціле число без знаку, яке ПОВИННО вказувати розмір у байтах вільного простору, визначеного списком вільних фрагментів.

`guidFileVersion (16 байт):` GUID. Коли змінюється значення поля **cTransactionsInLog** або поля **guidDenyReadFileVersion**, **guidFileVersion** НЕОБХІДНО змінити на новий GUID.

`nFileVersionGeneration (8 байтів):` Ціле число без знаку, яке вказує кількість змін у файлі. ПОВИННО збільшуватися, коли змінюється поле **guidFileVersion**.

`guidDenyReadFileVersion (16 байт):` GUID. Коли існуючий вміст файлу змінюється, за винятком структури **Header** файлу та невикористаних блоків зберігання, **guidDenyReadFileVersion** НЕОБХІДНО змінити на новий GUID.

`grfDebugLogFlags (4 байти):` МАЄ бути нульовим. НЕОБХІДНО ігнорувати.

`fcrDebugLog (12 байтів):` структура **FileChunkReference64x32**, яка ПОВИННА мати значення "fcrZero". НЕОБХІДНО ігнорувати.

`fcrAllocVerificationFreeChunkList (12 байтів):` Структура **FileChunkReference64x32**, яка ПОВИННА бути "fcrZero". НЕОБХІДНО ігнорувати.

`bnCreated (4 байти):` Ціле число без знаку, що вказує номер збірки програми, яка створила цей файл сховища версій. СЛІД ігнорувати.

`bnLastWroteToThisFile (4 байти):` Беззнакове ціле число, що вказує номер збірки програми, яка останньою записувала цей файл сховища версій. СЛІД ігнорувати.

`bnOldestWritten (4 байти):` Ціле число без знаку, яке вказує номер збірки найстарішої програми, яка записала цей файл сховища версій. СЛІД ігнорувати.

`bnNewestWritten (4 байти):` Ціле число без знаку, що вказує номер збірки останньої програми, яка записала цей файл сховища версій. СЛІД ігнорувати.

`rgbReserved (728 байтів):` МАЄ бути нульовим. НЕОБХІДНО ігнорувати.

## Посилання ##

* [[MS-ONESTORE] – формат файлу OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Вікіпедія](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)
