{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "файл", "расширение", "формат", "Электронная книга", "Цифровая книга" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла EPUB и API-интерфейсах, которые могут создавать и открывать файлы EPUB.",
  "title" :"Что такое файл EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## .EPUB вариант №

Файлы с расширением .epub представляют собой формат файлов электронных книг, который представляет собой стандартный формат цифровых публикаций для издателей и потребителей. К настоящему времени этот формат стал настолько распространенным, что поддерживается многими электронными книгами и программными приложениями. Например, в Mac OS предустановленное программное обеспечение **Books** поддерживает открытие таких файлов. Кроме того, существует множество совместимых программ для смартфонов, планшетов и компьютеров. Стандарты файлов EPUB поддерживаются [Международным форумом цифровых публикаций](https://idpf.org/epub/30/spec/epub30-publications.html) (IDPF). Версия EPUB 3 также одобрена Исследовательской группой книжной индустрии (BISG), ведущей ассоциацией книжной торговли для стандартизированных передовых практик, исследований, информации и мероприятий для упаковки контента.

## Краткая история формата файла EPUB

* **Октябрь 2007 г.** — утвержден формат EPUB 2.0.
* **Сентябрь 2010 г.** — выпущено техническое обновление
* **Октябрь 2011** — вступили в силу спецификации EPUB 3.0.
* **Июнь 2014 г.** — выпущено незначительное техническое обновление, заменяющее версию 3.0.
* **Январь 2017 г.** — EPUB 3.1 вступил в силу

## Формат файла EPUB

Формат файла EPUB представляет собой архив, который можно переименовать в расширение [ZIP](/ru/compression/zip/), а его содержимое можно просмотреть, распаковав архив любым архиватором. Это открытый формат на основе XML, состоящий из файлов HTML, изображений, таблиц стилей CSS и других элементов. Его также можно преобразовать в PDF, Mobi и несколько других форматов файлов с помощью ряда программных приложений и API.

{{< figure src="../epub.png" alt="Формат файла EPUB" >}}

**Электронная книга в формате EPUB, открытая с помощью приложения Mac OS Books**

Формат файла EPUB основан на следующих трех открытых стандартах.

### Открытая общественная структура (ОПС) ###

Файл EPUB 2.0 использует XHTML 1.1 для построения содержимого публикации. По сути это означает, что файл EPUB состоит из одной или нескольких веб-страниц. Несмотря на то, что вы можете включить все содержание книги или газеты на одной странице, лучше, чтобы такой файл не превышал 300 КБ, как по соображениям производительности, так и по соображениям совместимости. Как и в случае с обычными веб-страницами, стиль и макет определяются с помощью каскадных таблиц стилей (CSS). В файлах EPUB необходимо использовать подмножество (ограниченный набор команд) CSS2. Многие новые функции CSS3, такие как закругленные прямоугольники или тени, пока недоступны. Для обратной совместимости создатель также может использовать DTBook вместо XHTML для кодирования контента.

### Открытый формат упаковки (OPF) ###

Эта часть спецификации касается структурной информации, такой как метаданные (кто автор и издатель, каково название и т. д.), манифест (список всех файлов внутри файла epub) и оглавление. Все эти данные встраиваются с использованием XML.

### Формат открытого контейнера (OCF) ###

Как следует из вышеприведенного описания, документ EPUB состоит из набора файлов. Спецификации OCF определяют, как все эти файлы в конечном итоге упаковываются в один файл-контейнер. Для этого используется ZIP-сжатие.

## Поддерживаемые форматы файлов изображений ##

Формат файла EPUB поддерживает следующие форматы файлов изображений.

* [GIF](/ru/image/gif/)
* [JPG](/ru/image/jpeg/)
* [PNG](/ru/image/png/)
* [SVG](/ru/page-description-language/svg/)

## Использованная литература ##

* [EPUB — Википедия](https://en.wikipedia.org/wiki/EPUB)

