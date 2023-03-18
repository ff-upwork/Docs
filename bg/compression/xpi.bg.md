{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI – Междуплатформен пакетен файл за инсталиране",
  "description":"Научете за файловия формат XPI и API, които могат да създават и отварят XPI файлове.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Какво е XPI файл?

XPI файлът е инсталационен архив, който е компресиран, за да се намали размерът на файла. Използва се от приложения на Mozilla за инсталиране на плъгини и допълнителни файлове. Той съдържа инсталационен скрипт или манифест в основата на файла заедно с редица файлове с данни. XPI файл може да съдържа теми, набор от инструменти или добавки за Firefox, които потребителят може да инсталира, за да стане част от браузъра Firefox, Thunderbird или SeaMonkey.

## XPI файлов формат - повече информация

XPI файловете се записват на диск като [ZIP](/bg/compression/zip/) архиви, които комбинират множество файлове в един компресиран файл. Файловете в XPI файл може да включват инсталационен скрипт файл като JS и уеб файлове като [CSS](/bg/web/css/), [HTML](/bg/web/html/) и [JSON](/bg/web/json/ ). Понякога може също така да съдържа [PNG](/bg/image/png/) файлове с изображения, които да се използват като икони от добавката.

### Как да прегледам съдържанието на XPI файла?

XPI файл на практика е ZIP архив, чието съдържание може да се види чрез следните стъпки.

* Променете разширението на файла от XPI на ZIP
* Извлечете съдържанието на файла с помощта на стандартна помощна програма за декомпресия като WinZip (Windows, Mac), 7-Zip (Windows) или Apple Archive Utility (Mac).

### Инсталирайте XPI файл на Firefox Android

Повечето хора са любопитни да знаят дали XPI файловете могат да бъдат инсталирани във Firefox на устройства с Android. В Android можете да инсталирате добавка от XPI файл, като намерите файла и го отворите с Firefox.

## Препратки

* [XPInstall - Уикипедия](https://en.wikipedia.org/wiki/XPInstall)
* [Как мога да отворя файлово разширение XPI?](https://support.mozilla.org/en-US/questions/1009049)
