{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла QT — файл быстрого фильма",
  "keywords" :[ "QT", "QuickTime видео", "формат qt", "как воспроизводить файлы qt", "Quick Movie File", "QTFF", "видео", "Apple" ],
  "description":"Узнайте о формате файла QT и API-интерфейсах, которые могут создавать и открывать файлы QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## .QT вариант №

Файл с расширением .qt представляет собой мультимедийный файл-контейнер, который используется средой QuickTime для хранения содержимого мультимедийного файла. Формат файла QuickTime, разработанный Apple Inc. (QTFF), представляет собой мультимедийный файл-контейнер, который содержит аудио, видео или текст для последующего воспроизведения. Это предпочтительный формат для обмена цифровыми мультимедиа между устройствами, приложениями и операционными системами. Файлы QT также сохраняются в формате [MOV](/ru/video/mov/), который также был разработан Apple Inc. Некоторые из приложений, которые могут открывать файлы QT, включают Apple QuickTime player, VLC media player и Media Player Classic с K- Облегченный пакет кодеков.

## Формат файла QT

QTFF является объектно-ориентированным, предоставляя гибкую коллекцию объектов для простоты анализа и расширения. Каждая дорожка в файле QT содержит закодированный в цифровом виде медиапоток или ссылку на данные медиапотока, расположенного в другом файле. Иерархическая структура данных, состоящая из объектов, называемых атомами, действует как контейнеры дорожек. Спецификации формата файла для [формат файла QT](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) официально доступны Apple Inc для справки разработчика.

### Описание носителя

Описание мультимедиа файла QuickTime хранится отдельно от данных мультимедиа. Такая информация, как количество дорожек, формат сжатия видео и информация о времени, хранится в описании мультимедиа (также известном как ресурс фильма, атом фильма или просто фильм). На мультимедийные данные ссылается индекс в этой мультимедийной структуре. Медиаданные — это фактические образцы данных, такие как кадры видео и аудио, используемые в фильме.

### Атомы

Атом — это основная единица файла QuickTime. В любом атоме перед любым другим полем есть два основных поля: поля размера и типа. Поле размера показывает размер атома, а поле типа указывает тип данных, хранящихся в атоме. По своей природе атомы иерархичны, что означает, что один атом может содержать другие атомы, которые могут содержать другие. Схема образца атома показана на следующем изображении.

Каждый атом состоит из двух частей: заголовка и данных. Заголовок содержит поля размера и типа, а часть данных содержит фактические данные. Кроме того, каждое поле поясняется ниже:

#### Размер атома

Заголовок и содержимое атома указываются 32-битным целым числом, известным как размер атома. Поле размера содержит размер атома в байтах, выраженный в виде 32-битного целого числа без знака.

#### Тип атома

Тип атома также отображается 32-битным целым числом, которое в основном обрабатывается как четырехсимвольное поле с кнемоническим значением, например «moov» (0x6D6F6F76) для атома фильма или «trak» (0x7472616B) для атома фильма. трековый атом. Когда тип атома известен, это позволяет интерпретировать его данные.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Структура файла ##

Файлы QT/MOV состоят из последовательных фрагментов. Каждый чанк имеет 8-байтовый заголовок: 4-байтовый размер чанка (с обратным порядком байтов, старший байт вперед) и 4-байтовый тип чанка — одна из предопределенных сигнатур: «ftyp», «mdat», «moov», «pnot». ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", «клип», «crgn», «синхронизация», «глава», «tmcd», «scpt», «ssrc», «PICT». Первый фрагмент имеет тип "ftype" и имеет подтип по смещению 8. MOV определяется подтипом, который должен быть "qt". Чтобы составить файл MOV, необходимо повторять фрагменты до тех пор, пока не будет обнаружен неизвестный тип.

Вот пример: при просмотре двоичных данных образца файла MOV видно, что он начинается с подписи **ftyp** (шестнадцатеричный: 66 74 79 70) по смещению 4, которая определяет тип файла-контейнера QuickTime. Подтип файла — **qt~_~_** (hex: 71 74 20 20), что указывает на тип файла MOV. Размер первого блока равен 32 (шестнадцатеричный: 00 00 00 20, обратный порядок байтов, первый старший байт), размер расположен по смещению 0. По смещению 32 (шестнадцатеричный: 20) расположен второй блок, который имеет размер 8 и введите **mdat** (шестнадцатеричный: 6D 64 61 74).

Следующий фрагмент расположен по смещению 32+8#40 (шестнадцатеричный: 28), имеет размер 3 263 028 (шестнадцатеричный: 00 31 CA 34) и тип **mdat** (шестнадцатеричный: 6D 64 61 74) по смещению 44 (шестнадцатеричный : 2С). Следующий фрагмент расположен по смещению 40 + 3 263 028#3 263 068 (шестнадцатеричный: 00 31 CA 5C), имеет размер 21 189 (шестнадцатеричный: 00 00 52 C5) и тип **moov** (шестнадцатеричный: 6D 6F 6F 76) по смещению. 1 836 019 574 (шестнадцатеричный: 00 31 CA 60). Это последний фрагмент, поэтому общий размер файла составляет 3 263 068 + 21 189 # 3 284 257 байт.

## Использованная литература ##

* [Формат файла QT — Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)
* [Формат файла QuickTime — Википедия](https://en.wikipedia.org/wiki/QuickTime_File_Format)

