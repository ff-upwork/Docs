{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "файл", "расширение", "формат файла", "Макет страницы", "Инкапсулированный PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла EPS и API-интерфейсах, которые могут создавать и открывать файлы EPS.",
  "title" :"Формат файла EPS — инкапсулированный файл PostScript",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## .EPS вариант №

Файл .eps — это файл изображения, сохраняемый на диск в формате Encapsulated Postscript. Он может содержать любую комбинацию текста, графики и изображений. Файлы EPS могут также включать растровое изображение предварительного просмотра, инкапсулированное внутри для отображения приложениями, которые могут открывать такие файлы.

## Краткая история формата файла EPS

Беглый взгляд на формат файла EPS с точки зрения истории показывает следующую информацию:

* Первая версия EPS была выпущена Adobe где-то между 1985 и 1988 годами.
* Версия 2.0 спецификации EPS была опубликована в январе 1989 г.
* Спецификация EPS версии 3.0 была опубликована отдельным документом в 1992 г.; это последняя опубликованная версия.

EPS в сочетании с механизмом расширения Open Structuring Conventions, описанным в пункте 9 Спецификации Adobe PostScript Language Document Structuring Conventions, легли в основу ранних версий формата файла Adobe Illustrator Artwork.

## Формат EPS-файла

EPS является проприетарным, но общедоступным форматом, и спецификации формата файлов EPS доступны для разработчиков. EPS представляет собой формат файла, соответствующий [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention), и соответствует всем правилам, установленным DSC. DSC — это специальный формат файла для документов PostScript от Adobe. Любое приложение, которое утверждает, что может читать файлы EPS, должно быть совместимым с DSC.

Файл EPS состоит из двух основных разделов, как описано ниже.

### Изображение для предварительного просмотра ###

Типичный файл EPS содержит изображение для предварительного просмотра в формате, предназначенном для удобного использования в рабочем процессе, включающем несколько систем или приложений. Цель предварительного просмотра состоит в том, чтобы получить изображение в формате, который может отображать большинство графических приложений; предварительный просмотр обычно имеет более низкое разрешение, размер в пикселях и / или глубину в битах. Файл предварительного просмотра может быть в одном из нескольких форматов. Спецификация для EPS_3 перечисляет три формата предварительного просмотра «для конкретных устройств»:

* для Apple Macintosh изображение PICT, используемое приложением QuickDraw.
* для компьютеров DOS растровый файл TIFF
* Метафайл Windows.

PICT и Windows Metafile могут включать как растровые данные, так и векторную графику. Кроме того, спецификация определяет очень простое независимое от устройства представление встроенного растрового изображения предварительного просмотра. Это представление известно как Encapsulated PostScript Interchange Format (EPSI).

Предварительный просмотр EPSI представляет собой растровое изображение, представленное в шестнадцатеричном формате ASCII, заключенное между несколькими комментариями PostScript для идентификации и предназначенное для простоты и удобства переноса. Чтобы различать файлы EPS с различными форматами предварительного просмотра, в спецификации EPS были рекомендованы разные расширения файлов DOS и типы файлов Macintosh.

### Код PostScript

Как минимум, формат файла EPS должен включать следующее:

* комментарий заголовка, %!PS-Adobe-3.0 EPSF-3.0
* и комментарий ограничивающей рамки, %%BoundingBox: llx lly urx ury, описывающий границы иллюстрации. Эти четыре аргумента соответствуют нижнему левому (llx, lly) и верхнему правому (urx, ury) углам ограничивающей рамки.

Файл EPS не может использовать ни один из следующих операторов:

* полосовое устройство,
* очистить диктофон
* копия страницы
* стирание
* выходной сервер
* фреймустройство
* большой магазин
* инициализация
* инициализация
* матрица инициализации
* покидать
* рендербанды
* setglobal
* установка устройства
* setshared
* начало работы.

## Преобразование EPS в другие форматы файлов

Файлы EPS можно преобразовать в стандартные форматы изображений, такие как [JPG](/ru/image/jpeg/), [PNG](/ru/image/png/), [TIFF](/ru/image/tiff/) и [PDF](/ru/pdf). /) с использованием различных приложений, например Adobe Illustrator, Photoshop и PaintShop Pro.

Из-за [уязвимости системы безопасности](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) в файлах EPS, Office 2016, Office 2013, Office 2010 и Office 365 отключили возможность вставки файлов EPS в документы Office.

## использованная литература

* [Инкапсулированный PostScript — Википедия] (https://en.wikipedia.org/wiki/Encapsulated_PostScript)
