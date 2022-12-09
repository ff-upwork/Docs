{
  "date" : "2019-10-11",
  "keywords" :[ "html", "html файл", "формат файла html", "тип файла html", "файл", "тип", "что такое файл html" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла HTML",
  "description":"Узнайте о формате файла HTML и API, которые могут создавать и открывать файлы HTML.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Что такое HTML-файл?

HTML (Hyper Text Markup Language) — это расширение для веб-страниц, созданных для отображения в браузерах. HTML, известный как язык Интернета, развивался с учетом новых требований к информации, которая должна отображаться как часть веб-страниц. Последний вариант известен как HTML 5, что дает большую гибкость для работы с языком. HTML-страницы либо принимаются с сервера, на котором они размещены, либо также могут быть загружены из локальной системы. Каждая HTML-страница состоит из HTML-элементов, таких как формы, текст, изображения, анимация, ссылки и т. д. Эти элементы представлены тегами и несколькими другими, где каждый тег имеет начало и конец. Он также может встраивать приложения, написанные на языках сценариев, таких как JavaScript и таблицы стилей (CSS), для общего представления макета.

## Краткая история ##

С момента своего создания и первой роли спецификации HTML поддерживаются Консорциумом World Wide Web (W3C) с 1996 года. В 2000 году он также стал международным стандартом (ISO/IEC 15445:2000). В 1999 году был опубликован HTML 4.01. В 2004 году Рабочая группа по технологиям веб-гипертекстовых приложений (WHATWG) начала работу над версией HTML5, которая стала совместным результатом с W3C в 2008 году. Она была завершена и стандартизирована 28 октября 2014 года.

## Структура формата файла HTML ##

Документ HTML 4 состоит из трех частей:

1. строка, содержащая информацию о версии HTML
1. раздел декларативного заголовка
1. тело, содержащее фактическое содержание документа. Тело может быть реализовано элементом BODY или элементом FRAMESET, чтобы содержать тело в кадрах.

Каждый раздел может начинаться или сопровождаться пробелами, новыми строками, вкладками и комментариями. Пример простого HTML-документа показан ниже:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Информация о версии ###

Первая строка кода, \<!DOCTYPE html> , называется объявлением типа документа и сообщает браузеру, в какой версии HTML написана страница. В зависимости от версии HTML существует несколько различных объявлений типа документа, которые называют определение типа документа (DTD), используемое для документа. Каждое DTD отличается от других элементами, которые оно поддерживает, и отличается следующим образом:

* HTML 4.01 Strict — включает все элементы и атрибуты, которые не были [устарели] (https://www.w3.org/TR/html401/conform.html#deprecated) или не отображаются в документах с набором фреймов.
* HTML 4.01 Transitional — включает все в строгом DTD, а также устаревшие элементы и атрибуты (большинство из которых касается визуального представления
* HTML 4.01 Frameset — включает все элементы переходного DTD, а также фреймы.

Для **HTML5** информация о версии выглядит так, как указано ниже.

```
<!DOCTYPE html>
```

### Информация заголовка HTML ###

Заголовок документа HTML может включать ряд элементов HTML, которые не отображаются браузером. Такие элементы являются либо метаданными, описывающими информацию о странице, либо включают разделы, которые используются для получения информации из внешних ресурсов, таких как таблицы стилей CSS или файлы JavaScript. Заголовок страницы представлен тегом head.

Для установки заголовка страницы элемент **title** является единственным, который требуется в<head> теги. То же самое используется поисковыми системами для определения заголовка страницы.

### Информация о теле HTML ###

Это основной раздел файла, содержащий все содержимое файла, отображаемое браузерами. Тело HTML может содержать разметку, которая может ссылаться на различные стандартные блоки в виде тегов. Он может содержать несколько различных типов информации, таких как текст, изображения, цвета, графика и т. д. Кроме того, аудио- и видеоэлементы также могут быть встроены в тело html для отображения браузерами. При наличии современных таблиц стилей для визуального представления атрибуты представления BODY, такие как цвет фона, цвет ссылки, цвет текста и т. д., устарели. Таким образом, те же эффекты могут быть достигнуты с помощью таблиц стилей, как показано ниже:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Встроенные таблицы стилей легко встраиваются, а для быстрого применения визуальных эффектов внешние таблицы стилей упрощают однократное развертывание и доступ во многих местах.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML-элементы ###

Как упоминалось ранее, содержимое внутри тела HTML представлено тегами, также известными как элементы HTML. Каждый тег может иметь дополнительную информацию в виде атрибутов, которые записываются как<tag attribute1#"value1" attribute2#"value2"> , хотя нет необходимости иметь атрибуты для каждого тега. Если атрибуты не указаны, в каждом случае используются значения по умолчанию. Ниже приведены некоторые примеры элементов:

#### Заголовок ####

```
<head>
  <title>The Title</title>
</head>
```

#### Заголовки ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Пункты ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Использованная литература ##

* [Глобальная структура документа HTML] (https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)
