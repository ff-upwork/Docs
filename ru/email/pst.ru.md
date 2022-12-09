{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST — формат файла хранилища личной информации Outlook",
  "description":"Узнайте о формате файла PST и API, которые могут создавать и открывать файлы PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .PST вариант №

Файлы с расширением .pst представляют собой файлы личного хранилища Outlook (также называемые таблицей личного хранилища), в которых хранится разнообразная информация о пользователях. Информация о пользователе хранится в папках разных типов, включая электронные письма, элементы календаря, заметки, контакты и несколько других форматов файлов. Файлы PST используются для архивирования данных электронной почты в автономном режиме, которые впоследствии можно загружать и просматривать в различных приложениях.

## Спецификации формата файла PST

Формат файла PST [спецификации] (https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) доступен от Microsoft в качестве бесплатного и безотзывного бесплатного патентного лицензирования через Open Specification Promise. .

### Тип форматов PST

Форматы файлов PST подразделяются на два типа в зависимости от кодировки типа файла. Файлы PST с кодировкой ANSI являются старыми форматами файлов и поддерживаются только в Outlook 2002 и более ранних версиях. Такие файлы имеют максимальный размер 2 ГБ (2^^31^^ байт) и не поддерживают Unicode. Более современный тип формата файла, основанный на кодировке Unicode, снимает ограничение на размер файла и может достигать максимального размера данных 50 ГБ.

### Логическая организация формата файла PST

В основе формата файлов PST лежит B-дерево, которое упорядочивает данные и позволяет выполнять поиск, последовательный доступ, вставки, удаления и т. д. в логарифмическом масштабе. Общая структура файла PST состоит из трех слоев.

![Logical layers of a PST file](/ru/email/PST-1.png "Logical layers of a PST file")

«Уровень базы данных узлов (NDB)» — уровень базы данных узлов находится на нижнем уровне файла PST и включает базу данных узлов. Эти узлы фактически представляют собой низкоуровневые хранилища файлов формата PST. Уровень NDB состоит из заголовка, информации о размещении файлов, блоков и BT-деревьев (Node BTree и Block BTree) с точки зрения хранения. Узлы и блоки уровня NDB связаны через BID данных, который является одним из четырех свойств ссылки на узел, т.е. NID (идентификатор узла), NID родителя, BID данных (BID блока) и BID подузла.

Уровень списков, таблиц и свойств — уровень LTP обеспечивает логическое понимание концепций более высокого уровня поверх NDB. Помимо других элементов, уровень LTP в основном состоит из контекста свойств (PC) и контекста таблицы (TC). PC представляет собой набор свойств, а TC представляет собой двумерную матрицу набора свойств и их наличия. Эффективная реализация ПК и ТС, уровень LTP использует следующие два типа структур данных поверх узла NDB:

* Heap On Node (HN) — позволяет распределять поток данных узла на небольшие фрагменты переменного размера.
* BTree on Heap (BTH) - BTH обеспечивает удобный и практичный способ поиска по данным. PC, описанные выше, реализованы как BTH и поэтому реализованы путем построения внутри структуры HN.

«Уровень обмена сообщениями» — на этом уровне реализованы правила и бизнес-логика более высокого уровня для работы с файлами PST. Логический вывод этого уровня приводит к объектам «Папка», объектам «Сообщение», объектам «Вложения» и «Свойствам», что стало возможным благодаря объединению слоев LTP и NDB. На этом уровне также определяются правила и требования, которым необходимо следовать при изменении содержимого PST.

### Физическая организация формата файла PST

Высокий уровень файловой организации PST-файла показан на рисунке ниже. Это просто обзор различных концепций логических элементов файла PST.

![Physical organization of the PST file format](/ru/email/PST-2.png "Physical organization of the PST file format")


#### Информация заголовка PST

Структура HEADER файла PST расположена в самом начале файла по смещению 0. Он содержит информацию метаданных о файле PST и информацию ROOT для доступа к структурам данных уровня NDB, описанным выше. Структура HEADER различается для версий формата PST файлов Unicode и ANSI.

Заголовок начинается с 4-байтового магического слова **!BDN**, представленного байтами (0x21, 0x42, 0x44, 0x4E). Еще одно 2-байтовое магическое число, **SM** (0x53, 0x4D), расположено по смещению 8 от начала файла. Информация о версии (ANSI или Unicode) находится со смещением 10 от начала файла. Шестнадцатеричное значение (0x17) указывает файл Unicode PST, а 0x0E или 0x0F представляет формат файла ANSI.

|Поле|Описание
---|---|
|dwMagic (4 байта)|ДОЛЖЕН быть "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 байта)|32-битное значение CRC из 471 байта данных, начиная с wMagicClient (0ffset 0x0008)
|wMagicClient (2 байта)|ДОЛЖЕН быть "{0x53, 0x4D}".
|wVer (2 байта)|Версия формата файла. Это значение ДОЛЖНО быть 14 или 15, если файл является файлом ANSI PST, и ДОЛЖНО быть 23, если файл является файлом Unicode PST.
|wVerClient (2 байта)|Версия формата файла клиента. Версия, соответствующая формату, описанному в этом документе, — 19. Создателям нового PST-файла на основе этого документа СЛЕДУЕТ инициализировать это значение равным 19.
|bPlatformCreate (1 байт)|Это значение ДОЛЖНО быть установлено на 0x01.
|bPlatformAccess (1 байт)|Это значение ДОЛЖНО быть установлено на 0x01.
|dwReserved (8 байт)|
|bidUnused (только 8 байт Unicode)|Неиспользуемое заполнение добавлено при создании формата файла Unicode PST.
|bidNextP (Unicode: 8 байтов; ANSI: 4 байта)|BID следующей страницы. Страницы имеют специальный счетчик для распределения значений bidIndex. Из этого счетчика выделяется значение bidIndex для BID для страниц.
|bidNextB (только 4 байта ANSI): |Следующая ставка. Это значение является монотонным счетчиком, который указывает BID, который будет назначен для следующего выделенного блока. Значения BID увеличиваются с шагом 4. Дополнительные сведения см. в разделе 2.2.2.2.
|dwUnique (4 байта)|Это монотонно возрастающее значение, которое изменяется каждый раз при изменении структуры HEADER файла PST. Функция этого значения состоит в том, чтобы предоставить уникальное значение и гарантировать, что CRC HEADER различны после каждой модификации заголовка.
|rgnid[] (128 байт)|Фиксированный массив из 32 NID, каждый из которых соответствует одному из 32 возможных NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwUnused (8 байт)|Неиспользуемое пространство; ДОЛЖЕН быть установлен на ноль. Только в формате Unicode PST.
|root (Unicode: 72 байта; ANSI: 40 байтов)|КОРНЕВАЯ структура (раздел 2.2.2.5).
|dwAlign (4 байта)|Неиспользуемые байты выравнивания; ДОЛЖЕН быть установлен на ноль. Только в формате Unicode PST.
|rgbFM (128 байт)|Устаревший FMap. Это больше не используется и ДОЛЖНО быть заполнено 0xFF. Читатели ДОЛЖНЫ игнорировать значение этих байтов.
|rgbFP (128 байт)|Устаревший FPMap. Это больше не используется и ДОЛЖНО быть заполнено 0xFF. Читатели ДОЛЖНЫ игнорировать значение этих байтов.
|bSentinel (1 байт)|ДОЛЖЕН иметь значение 0x80.
|bCryptMethod (1 байт)|Указывает, как кодируются данные в файле PST. ДОЛЖНО быть установлено одно из предопределенных значений (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserved (2 байта)| Сдержанный; ДОЛЖЕН быть установлен на ноль.
|bidNextB (8 байт)|Указывает следующее доступное значение BID. Только в формате Unicode PST.
|bidNextB (ТОЛЬКО Unicode: 8 байт)|Следующая ставка. Это значение является монотонным счетчиком, который указывает BID, который будет назначен для следующего выделенного блока. Значения BID увеличиваются с шагом 4. Дополнительные сведения см. в разделе 2.2.2.2.
|dwCRCFull (4 байта)|32-битное значение CRC из 516 байтов данных, начиная с wMagicClient и заканчивая bidNextB включительно. Только в формате Unicode PST.
|ullReserved (8 байт)|Зарезервировано; ДОЛЖЕН быть установлен на ноль. Только формат файла ANSI PST.
|dwReserved (4 байта)|Зарезервировано; ДОЛЖЕН быть установлен на ноль. Только формат файла ANSI PST.
|rgbReserved2 (3 байта)|
|bЗарезервировано (1 байт) |
|rgbReserved3 (32 байта) |

### Защита данных ###

В целях безопасности файлы PST также могут быть защищены паролем, что требует, чтобы загрузочное приложение применяло пароль, прежде чем его можно будет просмотреть. Пароль, примененный к файлу PST, хранится в хранилище сообщений. Однако это не обеспечивает надежной защиты данных, поскольку пароль можно удалить с помощью доступных средств. Кроме того, указанный пользователем пароль не используется как часть ключа для кодирования и декодирования алгоритмов шифрования. Таким образом, защита данных, к которым могут получить доступ неавторизованные стороны, бесполезна. Хранение пароля в виде хэша CRC-32 исходной строки также делает его слабым методом защиты данных от грубой силы.

## Использованная литература ##

* [Формат файла личных папок Outlook (.pst)] (https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Спецификации формата файлов личных папок] (https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)
