---
date: 2020-08-12
keywords: jfif, .jfif, формат файла jfif, как открыть файлы jfif, расширение .jfif, расширение jfif
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Файл JFIF — что такое файл .jfif?
linktitle: JFIF
description: "Узнайте о формате файлов JFIF и API, которые могут создавать и открывать файлы JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## .JFIF вариант №

JFIF (формат обмена файлами JPEG (JFIF)) — это файл формата изображения с расширением .jfif. JFIF строится поверх JIF (формата обмена JPEG), уменьшая сложность и устраняя его ограничения.

## Краткая история JFIF

Разработкой документа JFIF руководил Эрик Гамильтон, и соглашение по первой версии было заключено в конце 1991 года. Версия 1.02 была опубликована 7 сентября 1992 года. В RFC 2046 указано, что формат JFIF используется для передачи изображений JPEG через Интернет. JFIF был опубликован ECMA в 2009 г. и стандартизирован ITU-T в 2011 г. как его Рекомендация T.871 и ISO/IEC в 2013 г. как ISO/IEC 10918-5.

## Формат файла JFIF ##

Файл JFIF состоит из последовательности маркеров, как определено в части 1 стандарта JPEG. Каждый маркер состоит из двух байтов (FF, за которым следует байт, указывающий тип маркера). Маркеры могут быть либо автономными, либо указывать начало сегмента маркера.

JFIF позволяет нескольким компонентам, таким как Y, Cb, Cr, иметь разное разрешение, но их выравнивание не определено. В отличие от JPEG, JFIF может предоставлять информацию о разрешении и соотношении сторон. JFIF также определяет используемую цветовую модель.

### Структура файла ##

|Сегмент|Код|Описание|
|---|---|---|
|SOI|FF D8|Начало изображения|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|дополнительные сегменты маркера|
|SOS|FF DA|Начало сканирования|
||сжатые данные изображения||
|EOI|FF D9|Конец изображения|

Стандарт JFIF определяет следующие сегменты:

### Сегмент маркера JFIF APP0 ###

Это обязательный сегмент, содержащий параметры изображения. Он также может содержать встроенную несжатую миниатюру.

|Поле|Размер (байты)|Описание|
|---|---|---|
|Маркер APP0|2|FF E0|
|Длина|2|Длина сегмента без маркера APP0|
|Идентификатор|5|JFIF (4A 46 49 46 00) в ASCII, оканчивающийся нулевым байтом|
|Версия JFIF|2|Версия JFIF|
|Единицы плотности|1|Единица для следующих полей плотности пикселей</br> 00 : Нет единиц; соотношение сторон ширина:высота в пикселях равно Ydensity:Xdensity</br> 01: пикселей на дюйм</br> 02 : Пикселей на сантиметр |
|Xdensity|2|Горизонтальная плотность пикселей больше нуля|
|Ydensity|2|Вертикальная плотность пикселей больше нуля|
|Xthumbnail|1|Горизонтальное количество пикселей встроенной миниатюры RGB. Может быть ноль|
|Ythumbnail|1|Вертикальное количество пикселей встроенной миниатюры RGB. Может быть ноль|
|Эскизы данных|3 × n|Несжатые 24-битные растровые данные миниатюр RGB|

### Сегмент маркера APP0 расширения JFIF ###

Это необязательный раздел, который, если он определен, должен следовать сразу за сегментом маркера JFIF APP0. Этот раздел поддерживается JFIF версии 1.02 и выше и позволяет встраивать эскизы в трех различных форматах.

|Поле|Размер (байты)|Описание|
|---|---|---|
|Маркер APP0|2|FF E0|
|Длина|2|Длина сегмента без маркера APP0|
|Идентификатор|5|JFXX (4A 46 58 58 00) в ASCII, оканчивающийся нулевым байтом|
|Формат миниатюры|1|Указывает, какой формат данных используется для следующей встроенной миниатюры:</br> 10 : Формат JPEG</br> 11: формат палитры 1 байт на пиксель</br> 13: 3 байта на пиксель в формате RGB|
|Эскиз данных|переменная||

## Преобразование JFIF в другие форматы файлов изображений

JFIF можно преобразовать в популярные форматы файлов изображений, такие как [PNG](/ru/image/png/), [JPG](/ru/image/jpg/) и [PDF](/ru/pdf/).

## Использованная литература ##

- [JFIF - Википедия] (https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)
