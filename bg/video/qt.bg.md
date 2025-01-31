{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QT файлов формат - Бърз филмов файл",
  "keywords" :[ "QT", "QuickTime видео", "qt формат", "как да възпроизвеждам qt файлове", "Бърз филмов файл", "QTFF", "видео", "Apple" ],
  "description":"Научете за QT файловия формат и API, които могат да създават и отварят QT файлове.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Какво е QT файл?

Файл с разширение .qt е файл с мултимедиен контейнер, който се използва от рамката QuickTime за съхраняване на съдържанието на мултимедиен файл. Разработен от Apple Inc. QuickTime File Format (QTFF) е мултимедиен контейнерен файл, който съдържа аудио, видео или текст за възпроизвеждане по-късно. Това е избраният формат за обмен на цифрови медии между устройства, приложения и операционни системи. QT файловете също се записват във формат [MOV](/bg/video/mov/), който също е разработен от Apple Inc. Някои от приложенията, които могат да отварят QT файлове, включват Apple QuickTime player, VLC media player и Media Player Classic с K- Lite Codec Pack.

## QT файлов формат

QTFF е обектно-ориентиран, който излага гъвкава колекция от обекти за улесняване на анализиране и разширяване. Всяка песен в QT файл съдържа цифрово кодиран медиен поток или препратка към данни към медийния поток, намиращ се в друг файл. Йерархичната структура от данни, състояща се от обекти, наречени атоми, действа като контейнери за следи. Спецификациите на файловия формат за [файлов формат QT](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) са официално достъпни от Apple Inc за справка от разработчиците.

### Описание на медията

Медийното описание на файл QuickTime се съхранява отделно от медийните данни. Информация като броя на песните, формата на видео компресия и информацията за времето се съхранява в медийното описание (известно още като филмов ресурс, филмов атом или просто филм). Медийните данни се посочват от индекс в тази медийна структура. Медийните данни са действителните примерни данни, като например видео кадри и аудио проби, използвани във филма.

### Атоми

Atom е основната единица на файла QuickTime. Има две основни полета във всеки атом преди всяко друго поле: полета за размер и тип. Полето за размер показва размера на атома, докато полето за тип показва типа данни, съхранявани в атома. По природа атомите са йерархични, което означава, че един атом може да съдържа други атоми, които пак могат да съдържат други. Оформлението на примерен атом е показано на следното изображение.

Всеки атом има две части, заглавка и данни. Заглавката съдържа полетата за размер и тип, а частта с данни съдържа действителните данни. Освен това всяко поле е обяснено по-долу:

#### Размер на атома

Заглавието и съдържанието на атома се обозначават с 32-битово цяло число, известно като размера на атома. Полето за размер съдържа размера на атома в байтове, изразен в 32-битово цяло число без знак.

#### Тип атом

Типът на атома също се показва от 32-битово цяло число, което най-често се третира като поле от четири знака с кнемонична стойност, като например „moov“ (0x6D6F6F76) за филмов атом или „trak“ (0x7472616B) за писта атом. След като типът на атома е известен, той позволява интерпретиране на неговите данни.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Файлова структура ##

QT/MOV файловете се състоят от последователни парчета. Всяка част има 8-байтово заглавие: 4-байтов размер на част (big-endian, старши байт първи) и 4-байтов тип на част - един от предварително дефинираните подписи: "ftyp", "mdat", "moov", "pnot" ", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Първата част е от тип „ftype“ и има подтип при отместване 8. MOV, дефиниран от подтип, който трябва да бъде „qt“. За съставяне на MOV файл е необходимо повтаряне на парчета, докато не бъде открит неизвестен тип.

Ето примерен пример: При проверка на двоичните данни на примерен MOV файл е очевидно, че той започва със сигнатура **ftyp** (шестнадесетичен: 66 74 79 70) при отместване 4, което дефинира Типа файл на контейнер QuickTime. Подтипът на файла е **qt~_~_** (шестнадесетичен: 71 74 20 20), което сочи към файлов тип MOV. Първият размер на блока е 32 (шестнадесетичен: 00 00 00 20, голям порядък, старши байт първи), размерът се намира при отместване 0. При отместване 32 (шестнадесетичен: 20) се намира втората част, която има размер 8 и тип **mdat** (шестнадесетичен: 6D 64 61 74).

Следващата част се намира на отместване 32+8#40 (шестнадесетичен: 28) и има размер 3,263,028 (шестнадесетичен: 00 31 CA 34) и тип **mdat** (шестнадесетичен: 6D 64 61 74) на отместване 44 (шестнадесетичен : 2C). Следващата част се намира при отместване 40 + 3,263,028#3,263,068 (шестнадесетичен: 00 31 CA 5C) и има размер 21,189 (шестнадесетичен: 00 00 52 C5) и тип **moov** (шестнадесетичен: 6D 6F 6F 76) при отместване 1,836,019,574 (шестнадесетичен: 00 31 CA 60). Това е последната част, така че общият размер на файла е 3,263,068+21,189#3,284,257 байта.

## Препратки ##

* [QT файлов формат - Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)
* [Файлов формат QuickTime – Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

