{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла TEX",
  "description":"Узнайте о формате файлов TEX и API, которые могут создавать и открывать файлы TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## .TEX вариант № ##

**TeX** — это язык, который включает в себя функции программирования, а также функции разметки, используемые для набора документов. Дональд Кнут из Стэнфордского университета является создателем этой находчивой системы набора текста. Во всем мире TeX — лучший выбор авторов и издателей для создания высококачественной технической документации. TeX отлично справляется с форматированием сложных математических выражений. В сочетании с высококачественным фотонаборным устройством TeX конкурирует с результатами, полученными с помощью лучших традиционных систем набора текста. Поэтому считается самой классной цифровой типографской системой.

Входные файлы TeX основаны на коде ASCII, что позволяет совместно использовать рукописи писателям, менеджерам издательств и критикам. Широкий спектр вычислительных сред, почти каждая современная платформа и множество старых платформ поддерживают TeX. Более того, TeX является бесплатным программным обеспечением, доступным широкому кругу потребителей. Многие установки UNIX используют как UNIX troff, так и TeX в качестве системы форматирования для разных целей. Другие задачи по набору текста выполняются с помощью LaTeX, ConTeXt и других пакетов макросов.

## Краткая история ##

TeX был разработан и написан Дональдом Кнутом в 1978 году. Гай Стил из Массачусетского технологического института переработал ввод/вывод TeX, чтобы заставить его работать в несовместимой операционной системе, такой как система разделения времени (ITS). Первая версия TeX была разработана под стэнфордской операционной системой WAITS на языке программирования (SAIL) и протестирована для работы на PDP-10. Кнут представил идею грамотного программирования для продвинутых версий. Грамотное программирование — это способ создания компилируемого исходного кода и набора (в TeX) документации с перекрестными ссылками с использованием исходного файла. Язык, используемый для разработки этих расширенных версий TeX, называется WEB и представляет собой смесь программ DEC PDP-10 Pascal для обеспечения переносимости.

Пересмотренная новая версия TeX, опубликованная в 1982 году, называлась TeX82. Основным изменением является замена исходного алгоритма расстановки переносов недавно написанным алгоритмом Фрэнка Лианга. Чтобы обеспечить переносимость между различными платформами, вместо использования с плавающей запятой TeX82 использует арифметику с фиксированной запятой вместе с настоящим полным по Тьюрингу языком программирования. В 1989 году были выпущены новые версии TeX и Metafont. Таким образом, версия TeX 3.0 поддерживает 8-битный ввод, позволяя использовать в тексте 256 различных символов. После версии 3 обновления обозначаются добавлением дополнительной цифры в конце десятичного числа, например, текущая версия TeX указывается как 3.14159265. Последняя версия была обновлена 12-1-2014.

## Ввод TeX ##

Входной файл для TEX может быть подготовлен в текстовом редакторе с использованием обычного текста. В отличие от обычного текстового процессора, этот входной файл запрещает использование любых невидимых управляющих символов. Один файл может быть встроен в другой файл, содержащий определения макросов и вспомогательные определения, что расширяет возможности TeX. Если установка TeX поставляется с какими-либо файлами макросов, локальная информация о TeX демонстрирует использование файлов макросов. Стандартная форма TeX объединяет комбинацию макросов и других определений, известную как простой TEX.

На основе точного знания размеров всех знаков и символов он рассчитывает оптимальную организацию букв в строке и строк на странице. Во время обработки документа создается файл .dvi, где «dvi» означает «независимый от устройства». Программы драйверов устройств необходимы для печати или предварительного просмотра документа с расширением dvi. В настоящее время генерация dvi обходится широко используемым pdf-TeX. При установке TeX нет предварительных знаний о шрифтах, поэтому для получения информации для документа используются внешние файлы шрифтов, которые являются частью локальной среды TeX.

## Система набора ##

Базовая система TeX может понять около 300 примитивов (команд). Примитивы являются низкоуровневыми командами, поэтому обычный пользователь редко использует их напрямую, и большая часть функций выполняется файлами форматирования. Эти файлы формата представляют собой предварительно загруженные в память образы TeX, за которыми следует загрузка больших коллекций макросов. Исходный формат языка по умолчанию, то есть простой TeX, добавляет около 600 команд.

Обратная косая черта, сгруппированная с фигурными скобками, обозначает запуск команд TeX. Поскольку TeX - это язык, основанный на макросах и токенах, почти все синтаксические характеристики TeX могут быть изменены во время выполнения, включая определяемые пользователем, за исключением нерасширяемых токенов, которые затем выполняются. Расширение само по себе практически без проблем. Некоторые команды должны идти после аргументов, которые помогают объяснить функцию команды. Например, команда \vskip предписывает TEX пропустить страницу вниз/вверх, за которой следует аргумент, определяющий, сколько места нужно пропустить.

## Версии ##

LaTeX — наиболее часто используемый формат, изначально разработанный Лесли Лэмпорт. LaTeX интегрирует различные стили документов для файлов, писем, книг и слайдов и предлагает ссылки и автоматическую нумерацию для различных разделов и математических выражений. AMS-TeX — еще один популярный формат, разработанный Американским математическим обществом.

AMS-TeX предлагает гораздо больше удобных для пользователя команд, которые могут быть переопределены журналами в соответствии с их местным стилем. LaTeX может воспользоваться преимуществами AMS-TeX, используя «пакеты» AMS, которые затем называются AMS-LaTeX. ConTeXt — это еще один формат, написанный Хансом Хагеном и используемый в основном для настольных издательских систем.

Программное обеспечение TeX предлагает несколько функций, которые были недоступны или имели более низкое качество в других системах набора текста на момент его создания. Некоторые из новаторских особенностей этого языка основаны на интересных алгоритмах, полученных из тезисов учеников Кнута. В то время как другие программы для набора текста теперь включают в свои программы полезные функции TeX.

## Использованная литература ##

* [Система набора текста TeX](https://en.wikipedia.org/wiki/TeX)

