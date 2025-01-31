{
  "date" : "2019-10-11",
  "keywords" :[ "webp файл", "webp файлов формат", "какво е webp файл", "файл", "webp пример", "webp файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP – файлов формат за растерни изображения на Google",
  "description":"Научете за WEBP файловия формат и API, които могат да създават и отварят WEBP файлове.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е WEBP файл?

WebP, въведен от Google, е модерен формат за растерни уеб изображения, който се основава на компресия без загуби и компресия със загуби. Той осигурява същото качество на изображението, като същевременно значително намалява размера на изображението. Тъй като повечето от уеб страниците използват изображения като ефективно представяне на данни, използването на WebP изображения в уеб страниците води до по-бързо зареждане на уеб страниците. Според Google, WebP изображенията без загуба са с 26% по-малки по размер в сравнение с [PNG](/bg/image/png/), докато WebP изображенията със загуба са 25-34% по-малки от сравнимите [JPEG](/bg/image/jpeg/) изображения. Изображенията се сравняват въз основа на индекса за структурно сходство (SSIM) между WebP и други файлови формати на изображения. WebP е дъщерен проект на [WebM](https://en.wikipedia.org/wiki/WebM) формат на мултимедиен контейнер.

## Преглед на функциите на WebP ##

WebP изображенията използват процеса на компресия, базиран на прогнозирането на пиксели от заобикалящите ги блокове, което води до използване на пиксели многократно в един файл. Той поддържа анимирани изображения и се очаква да поддържа повече функции в бъдеще. Google предостави изходния код [онлайн](https://developers.google.com/speed/webp/download) за своя енкодер и декодер, така че да се използва, когато е необходимо. WebP изображението осигурява поддръжка за:

* **Компресия със загуби:** Компресията със загуби се основава на [VP8](https://en.wikipedia.org/wiki/VP8) кодиране на ключови кадри. VP8 е формат за видео компресия, създаден от On2 Technologies като наследник на форматите VP6 и VP7.
* **Компресия без загуби:** Форматът за компресия без загуби е разработен от екипа на WebP.
* **Прозрачност:** 8-битовият алфа канал е полезен за графични изображения. Алфа каналът може да се използва заедно с RGB със загуби, функция, която в момента не е налична с никой друг формат.
* **Анимация:** Поддържа анимирани изображения с истински цветове.
* **Метаданни:** Може да има EXIF и XMP метаданни (използвани от камери, например).
* **Цветов профил:** Може да има вграден ICC профил.

WebP компресията със загуби използва предсказуемо кодиране за кодиране на изображение, същият метод, използван от видео кодека VP8 за компресиране на ключови кадри във видеоклипове. Предсказуемото кодиране използва стойностите в съседни блокове от пиксели, за да предвиди стойностите в блок, и след това кодира само разликата.

WebP компресията без загуби използва вече видени фрагменти от изображението, за да реконструира точно нови пиксели. Може също да използва локална палитра, ако не бъде намерено интересно съвпадение.

## Файлов формат ##

Файловият формат WebP се основава на документа RIFF (файлов формат за обмен на ресурси). Контейнерът WebP осигурява поддръжка за над и над функциите, освен да съдържа само едно изображение, кодирано като VP8 ключов кадър. Основният елемент на RIFF файл е част, която се състои от:


|Поле|Описание
---|---|
|Chunk FourCC: 32 бита|ASCII четирисимволен код, използван за идентификация на парче
|Размер на парчето: 32 бита (uint32)|Размерът на парчето, без това поле, идентификаторът на парчето или подложката
|Полезен товар на частта: Размер на частта в байтове|Полезният товар на данните. Ако размерът на парчето е нечетен, се добавя един байт за допълване ~-~-, който трябва да бъде 0 ~-~-
|ChunkHeader ('ABCD')|Използва се за описание на FourCC и заглавката на размера на парчето на отделни парчета, където 'ABCD' е FourCC за парчето. Размерът на този елемент е 8 байта.

### WebP Header ###

Хедърът на WebP файл е както следва:

* RIFF Header - 32 бита, представляващи ASCII символите 'R' 'I' 'F' 'F'
* Размер на файла - 32 бита (uint32), представляващ размера на файла в байтове, започвайки от отместване 8. Максималната стойност на това поле е 2^32 минус 10 байта и по този начин размерът на целия файл е най-много 4GiB минус 2 байта .
* 'WEBP' - 32 бита, представляващи ASCII символите 'W' 'E' 'B' 'P'

### Файлов формат със загуба ###

WebP изображенията използват файловия формат със загуба, ако изображението е базирано на кодиране със загуба и не изисква разширени/разширени функции като прозрачност, анимация, алфа и др. Изображенията със загуба са по-малки и се поддържат и от по-старите приложения.

WebP файлът в този случай се състои от:

* 12 байта заглавка на WebP файл
* VP8 парче

[Ръководството за формат на данни и декодиране на VP8](https://tools.ietf.org/html/rfc6386) илюстрира спецификациите на формата на побитов поток на VP8.

### Файлов формат без загуба ###

Това оформление се използва, когато изображението е базирано на кодиране без загуби и няма нужда от разширените функции, предоставени от външния формат. По-старите приложения обаче може да не могат да четат такива файлове.

WebP файлът в този случай се състои от:

* 12 байта заглавка на WebP файл
* VP8L парче

## Препратки ##

* [Справочник на разработчици на WebP - от Google](https://developers.google.com/speed/webp/)
* [WebP файлов формат - от Wikipedia](https://en.wikipedia.org/wiki/WebP)

