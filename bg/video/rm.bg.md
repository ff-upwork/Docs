---
date: 2019-10-11
keywords: rm, .rm, файлов формат rm, файлов формат .rm, разширение .rm, файлов формат RealMedia
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Научете за RM файловия формат и API, които могат да създават и отварят RM файлове."
title: RM файлов формат
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Какво е RM файл? ##

RealMedia е патентован мултимедиен контейнерен формат, разработен от RealNetworks, който използва разширението .rm. Използва се с комбинация от [RealAudio (RA)](/bg/audio/ra/) и [RealVideo(RV)](/bg/video/rv/) за поточно предаване през интернет. Тези потоци са с постоянен битрейт. За променлив битрейт RealNetworks разработи формата RealMedia Variable Bitrate (RMVB). RealMedia е подходящ за поточно предаване на съдържание през интернет и може да се използва например за поточно предаване на телевизия на живо.

## Структура на файла RealMedia ##

Файлът RealMedia се състои от поредица от части, всяка от които има следната структура:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

По-долу са типовете парчета, присъстващи във файла RealMedia:

- **Header на RealMedia файл (.RMF)**: Това трябва да е първото парче във файла RealMedia. В един файл присъства само една RMF част. Съдържа информация за броя на заглавките.
- **Заглавка на свойствата на файла (PROP)**: Това съдържа информация за общите свойства на файла RealMedia. Във всеки файл на RealMedia има само една част от този тип.
- **Заглавка на медийни свойства (MDPR)**: Тази част съдържа информация за свойствата на потока. Той съдържа информация за вида на потока и използвания кодек. Има едно MDPR парче за всеки поток във файла.
- **Заглавка на описанието на съдържанието (CONT)**: Тази част съдържа текстова информация като заглавието или автора на съдържанието във файла RealMedia. Тази част е само за информационни цели.
- **Заглавка на данни (DATA)**: Тази част съдържа група пакети с данни.
- **Заглавка на индекс (INDX)**: Тази част идва след всички части DATA и съдържа записи в индекса. Един файл може да има повече от един INDX блок.

## Поддържани аудио и видео формати ##

### Аудио формати ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- готвач: готвач
- atrc: ATRAC3
- ralf: RealAudio Lossless Format
- raac: LC-AAC
- racp: HE-AAC

### Видео формати ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 предшественик
- RV40: H.264 предшественик, RV40
- RVTR: H.263+ (RV20)

## Препратки ##

- [RealMedia - Уикипедия](https://en.wikipedia.org/wiki/RealMedia)

