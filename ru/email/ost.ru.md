{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST — формат файла хранилища Outlook",
  "description":"Узнайте о формате файлов OST и API-интерфейсах, которые могут создавать и открывать файлы OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## OST вариант №

OST или файлы автономного хранилища представляют данные почтового ящика пользователя в автономном режиме на локальном компьютере после регистрации на сервере Exchange с использованием Microsoft Outlook. Он автоматически создается при первом использовании Microsoft Outlook при подключении к серверу. После создания файла данные синхронизируются с сервером электронной почты, чтобы они были доступны в автономном режиме, а также в случае отключения от сервера электронной почты. Файлы OST могут использовать элементы почтового ящика, такие как электронные письма, контакты, информацию календаря, заметки, задачи и другие подобные данные. Пользователи могут создавать электронные письма и другие элементы данных в файле OST даже при отсутствии подключения к серверу, но они не будут синхронизированы с сервером. После установления соединения локальный файл снова синхронизируется с сервером, так что и сервер, и локальная копия находятся на одном уровне информации.

## Формат файла OST

Формат файлов OST (таблица автономного хранилища) и [PST](/ru/email/pst/) (таблица личного хранилища) состоит из формата файла личной папки (PFF), который соответствует хранению электронной почты, контактов и встреч пользователя. Данные в файле PFF хранятся с прямым порядком байтов, а все даты и время представлены как FILETIME в формате UTC. [MS-PST] определяет два типа PFF:

* 32-битный формат ANSI
* 64-битный формат Юникода

Формат файла PST [спецификации](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), доступный от Microsoft, также применим к формату файла OST как бесплатному и безотзывное патентное лицензирование через Open Specification Promise. Он состоит из следующих различимых элементов:

* Заголовок файла
* Данные заголовка файла
* Узел ветви индекса
* Листовой узел индекса
* (Файл) индекс смещения
* (Элемент) индекс дескриптора
* Локальные дескрипторы
* Тип таблицы элементов

### Информация заголовка

Структура HEADER файла OST расположена в самом начале файла по смещению 0. Он содержит информацию метаданных о файле OST и информацию ROOT для доступа к структурам данных уровня NDB, описанным выше. Структура HEADER различается для версий формата OST файлов Unicode и ANSI.

Заголовок начинается с 4-байтового магического слова **!BDN**, представленного байтами (0x21, 0x42, 0x44, 0x4E). Еще одно 2-байтовое магическое число, **SM** (0x53, 0x4D), расположено по смещению 8 от начала файла. Информация о версии (ANSI или Unicode) находится со смещением 10 от начала файла. Шестнадцатеричное значение (0x17) указывает файл OST Unicode, а 0x0E или 0x0F представляет формат файла ANSI.

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
|rgnid[]   (128 байт)|Фиксированный массив из 32 NID, каждый из которых соответствует одному из 32 возможных NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
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

## использованная литература

* [Формат файла личных папок Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Спецификации формата файлов личных папок](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

