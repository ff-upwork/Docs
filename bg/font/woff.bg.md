{
  "date" : "2020-08-20",
  "keywords" :[ "woff файл", "woff файлов формат", "какво е woff файл", "файл", "woff пример", "woff файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF – отворен файлов формат в мрежата",
  "description":"WOFF файлът е отворен формат на шрифт, създаден във формата на уеб отворен шрифт.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Какво е WOFF файл?

Файл с разширение .woff е файл с уеб шрифт, базиран на Web Open Font Format (WOFF). Той има компресиран контейнер, специфичен за формата, базиран на типове шрифтове TrueType (.TTF) или OpenType (.OTT). WOFF беше въведен с цел да се разграничат уеб шрифтовете от файловете с шрифтове, използвани в настолни приложения. В допълнение, форматът е насочен към намаляване на забавянето на прехвърлянето на шрифтове от сървъра към компютъра на клиента по мрежата. Налични са няколко инструмента, които могат да конвертират WOFF файлове в TTF и други файлови формати на шрифтове.

## **WOFF файлов формат**

Форматът на шрифт WOFF компресира таблици с данни за шрифтове на базирани на таблици sfnt структури, използвани в различни типове шрифтове като TrueType, OpenType и Open Font Format. Той е като контейнер за тези типове шрифтове и също така има място за включване на метаданните на шрифта и данните за лична употреба, които да бъдат включени в контейнера. Конверторите използват sfnt файловете във форматиран WOFF файл, а потребителските агенти възстановяват кодирания файл за използване с уеб документа. Трябва да се отбележи, че възстановените данни за шрифта съвпадат точно с формата на входния шрифт от всички аспекти.

Помощните програми за файлове на WOFF често съдържат допълнителни функции като поднабор на глифове, валидиране или добавяне на функции на шрифтове, но това не е необходимо. Както създателят, така и агентите на потребителя трябва да гарантират, че валидността на основните данни за шрифта е запазена.

### WOFF файлова структура

WOFF файловата структура е подобна на тази на sfnt шрифтовете. Базира се на директория с таблици, която съдържа дължините и отместванията на таблиците с данни за всеки шрифт. След тази първоначална информация следват всички таблици. Файлът съдържа база данни с шрифтове, които са същите като в оригиналните шрифтове. Редът на таблиците също е същият, но всяка може да бъде компресирана. Директорията на таблицата WOFF обаче замества оригиналната директория на таблицата.

WOFF файлът се състои от следното:

* WOFFHeader - Заглавка на файл с основен тип и версия на шрифта, заедно с отмествания към метаданни и блокове с лични данни.
* TableDirectory - Директория с таблици с шрифтове, посочваща оригиналния размер, компресирания размер и местоположението на всяка таблица в WOFF файла.
* FontTables - Таблиците с данни за шрифтове от входния sfnt шрифт, компресирани за намаляване на изискванията за честотна лента.
* ExtendedMetadata - Допълнителен блок от разширени метаданни, представени в XML формат и компресирани за съхранение във файла WOFF.
* PrivateData - незадължителен блок от лични данни, който дизайнерът на шрифтове, леярната или продавачът да използва.

### WOFF заглавка
Заглавието на WOFF се състои от идентификационен подпис, който показва вида на данните, включени във файла. Заглавието на WOFF заедно с неговите полета е както следва.

|Тип|Име на поле|Описание|
---|---|---|
|UInt32|подпис |0x774F4646 'wOFF' |
|UInt32| flavor |„sfnt версията“ на въведения шрифт.|
|UInt32| дължина |Общ размер на WOFF файла.|
|UInt16| numTables |Брой записи в директория с таблици с шрифтове.|
|UInt16| запазено | Запазено; настроен на нула.|
|UInt32| totalSfntSize |Общ размер, необходим за некомпресираните данни за шрифтове, включително sfnt заглавката, директорията и таблиците с шрифтове (включително подложки).|
|UInt16| majorVersion |Основна версия на WOFF файла.|
|UInt16| minorVersion |По-малка версия на файла WOFF.|
|UInt32| metaOffset |Отместване към блок с метаданни, от началото на WOFF файла.|
|UInt32| metaLength |Дължина на компресирания блок метаданни.|
|UInt32| metaOrigLength |Некомпресиран размер на блок метаданни.|
|UInt32| privOffset |Отместване към частен блок данни, от началото на WOFF файла.|
|UInt32| privLength |Дължина на частния блок от данни.|


## **Препратки**
* [w3 WOFF файлов формат](https://www.w3.org/TR/WOFF/)

