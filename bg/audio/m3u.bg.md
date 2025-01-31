---
date: 2019-12-13
keywords: m3u, m3u файлов формат, .m3u разширение, m3u мултимедиен плейлист, m3u плейлист формат
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Научете за файловия формат M3U и API, които могат да създават и отварят M3U файлове."
title: M3U файлов формат
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Какво е M3U файл? ##

M3U (MP3 URL) е файл с аудио плейлист, съхраняван с разширение .m3u. M3U не е истински аудио файл, той просто сочи към аудио и понякога видео файлове. M3U е разработен за използване със софтуер Winplay3 от Fraunhofer. Освен това се поддържа от различни медийни плейъри и софтуер.

## M3U файлов формат

Няма официална спецификация за файловия формат M3U, той е де факто стандарт. M3U е обикновен текстов файл, който използва разширението .m3u, ако текстът е кодиран в кодирането по подразбиране на локалната система, което не е Unicode, или с разширението .m3u8, ако текстът е кодиран UTF-8. Всеки запис във файла M3U може да бъде едно от следните:

- Абсолютен път до файла
- Път на файла спрямо файла M3U.
- URL

### Разширен M3U ###

В разширения M3U се въвеждат допълнителни директиви, които започват с "#" и завършват с двоеточие (:), ако имат параметри. По-долу е даден списък с директиви за разширен M3U.

- **#EXTM3U** - Това е заглавката на файла, указваща Extended M3U и трябва да бъде първият ред на файла.
- **#EXTENC:** - Кодиране на текст. Трябва да е вторият ред на файла.
- **#EXTINF:** - Използва се за информация за песни и други допълнителни свойства.
- **#PLAYLIST:** - Заглавието на плейлиста
- **#EXTGRP:** - Започнете групирането на имена
- **#EXTALB:** - Информация за албума
- **#EXTART:** - Изпълнител на албума
- **#EXTGENRE** - Жанр на албума
- **#EXTM3A** - Плейлист с един файл за песни или глави от албуми.
- **#EXTBYT:** - Размер на файла в байтове.
- **#EXTBIN:** - Следват двоични данни.
- **#EXTIMG:** - Лого, обложка или други изображения.

### HLS M3U ###

HLS (HTTP Live Streaming) е създаден от Apple за поточно предаване на аудио и радио към iOS устройства. Базиран е на UTF-8 кодиран разширен M3U. Той беше стандартизиран като RFC 8216 през 2017 г. от IETF. Етикетите за плейлиста HLS започват с "#EXT-X-". По-долу е даден списък с тагове за HLS

- **EXT-X-VERSION** - Показва версията за съвместимост на файла въз основа на носителя и неговия сървър.
- **#EXT-X-START:** - Показва предпочитаната начална точка за плейлиста.
- **#EXT-X-PLAYLIST-TYPE:** - Предоставя типа на плейлиста (СЪБИТИЕ или VOD).
- **#EXT-X-TARGETDURATION:** - Указва максималната продължителност на сегмента.
- **#EXT-X-MEDIA-SEQUENCE:** - Показва поредния номер на медията.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Показва, че всички медийни проби са независими и могат да бъдат декодирани без други сегменти.
- **#EXT-X-MEDIA:** - Използва се за свързване на медийни плейлисти, които съдържат алтернативни предавания на същото съдържание.
- **#EXT-X-STREAM-INF:** - Указва вариантен поток, който е част от предаванията.
- **#EXT-X-BYTERANGE:** - Показва, че медийният сегмент е поддиапазон на ресурса, идентифициран от неговия URI.
- **#EXT-X-DISCONTINUITY** - Показва прекъсване между предходните и следващите медийни сегменти.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Позволява синхронизиране между различни предавания на един и същ Вариантен поток или различни Вариантни потоци.
- **#EXT-X-KEY:** - Указва как да се дешифрират медийни сегменти.
- **#EXT-X-MAP:** - Указва как да се получи секция за инициализация на медиите. Изисква се анализ на приложимите медийни сегменти.
- **#EXT-X-PROGRAM-DATE-TIME:** - Свързва първата извадка от медийния сегмент с абсолютна дата и/или час.
- **#EXT-X-DATERANGE:** - Асоциира диапазон от данни.
- **#EXT-XI-FRAMES-ONLY** - Показва, че всеки медиен сегмент в плейлиста описва един I-кадър.
- **EXT-XI-FRAME-STREAM-INF** - Показва, че файлът с плейлиста съдържа I-кадри на мултимедийна презентация.
- **#EXT-X-SESSION-DATA:** - Позволява произволни данни за сесията
носени в главен плейлист.
- **#EXT-X-SESSION-KEY:** - Позволява ключове за криптиране. Клиентът може да зареди предварително тези ключове, без първо да прочете плейлиста.
- **#EXT-X-ENDLIST** - Показва, че към файла няма да се добавят повече медийни сегменти.

Следва списъкът с типове интернет медии, използвани от M3U:

- **application/vnd.apple.mpegurl**: Това е единственият регистриран тип медия (регистриран през 2009 г.) за M3U, който се използва за препратка към плейлистите в HLS приложенията.
- Следните типове интернет медии се използват от приложения, които не са HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Пример за M3U ##

Това е пример за файла M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Препратки ##

- [M3U - Уикипедия](https://en.wikipedia.org/wiki/M3U)
- [HTTP поточно предаване на живо](https://tools.ietf.org/html/rfc8216)

