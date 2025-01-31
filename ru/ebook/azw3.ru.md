{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "расширение", "файл", "формат", "электронная книга", "Формат файла Kindle", "Структура файла AZW3"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файлов AZW3 и API, которые могут создавать и открывать файлы AZW3.",
  "title" :"Что такое файл AZW3?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## .AZW3 вариант №

AZW3, также известный как Kindle Format 8 (**KF8**), представляет собой модифицированную версию формата цифровых файлов электронных книг [AZW](/ru/ebook/azw/), разработанную для устройств Amazon Kindle. Этот формат представляет собой усовершенствование старых файлов AZW и используется на устройствах Kindle Fire только с обратной совместимостью для исходного формата файлов, т.е. [MOBI](/ru/ebook/mobi/) и AZW. Amazon представила формат KFX (KF версии 10) после KF8, который используется на последних устройствах Kindle. Файлы AZW3 имеют тип интернет-медиа application/vnd.amazon.mobi8-ebook. Файлы AZW3 можно преобразовать в ряд других форматов файлов, таких как [PDF](/ru/pdf/), [EPUB](/ru/ebook/epub/), [AZW](/ru/ebook/azw/), [DOCX](/ru/ word-processing/docx/) и [RTF](/ru/word-processing/rtf/).

## Формат файла AZ3/KF8 ##

Файлы KF8 являются двоичными по своей природе и сохраняют структуру формата файла MOBI в виде файла PDB. Как упоминалось ранее, файл KF8 может состоять как из MOBI, так и из более новой версии KF8 EPUB позже. Внутренние детали формата были расшифрованы с помощью [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), который представляет собой скрипт Python, который анализирует окончательно скомпилированную базу данных и извлекает из нее исходные файлы MOBI или AZW. Файлы AZW3 (KF8) предназначены для версии EPUB3 с обратной совместимостью для EPUB. KF8 компилирует файлы EPUB и создает двоичную структуру на основе формата файла PDB.

## Использованная литература ##

* [KF8 — Википедия](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Распаковать Kindle](https://github.com/kevinhendricks/KindleUnpack)

