{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TEX файлов формат",
  "description":"Научете за файловия формат TEX и API, които могат да създават и отварят TEX файлове.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е TEX файл? ##

**TeX** е език, който включва функции за програмиране, както и функции за маркиране, използвани за набор на документи. Доналд Кнут от Станфордския университет е създателят на тази находчива система за набор. По целия свят TeX е най-добрият избор на автори и издатели за създаване на висококачествени технически документи. TeX изпълнява изключителна работа по форматиране на сложни математически изрази. Във връзка с висококачествена фотонабираща машина, TeX се конкурира с резултатите, генерирани от най-добрите традиционни системи за набор. Поради това се считат за най-класните цифрови типографски системи.

TeX входните файлове са базирани на ASCII-код, като по този начин позволяват споделяне на ръкописи между писатели, издателски мениджъри и критици. Голямо разнообразие от компютърни среди, почти всяка модерна платформа и много по-стари платформи поддържат TeX. Освен това TeX е безплатен софтуер, достъпен за широк кръг потребители. Много UNIX инсталации използват UNIX troff и TeX като система за форматиране за различни цели. Други задачи за набор се изпълняват изключително много под формата на LaTeX, ConTeXt и други макро пакети.

## Кратка история ##

TeX е проектиран и написан от Доналд Кнут през 1978 г. Гай Стийл от Масачузетския технологичен институт ревизира входа/изхода на TeX, за да може да работи под несъвместима операционна система като Timesharing System (ITS). Първата версия на TeX е разработена под операционната система WAITS на Станфорд на езика за програмиране (SAIL) и е тествана за работа на PDP-10. Кнут представи идеята за грамотно програмиране за напреднали версии. Грамотното програмиране е начин за генериране на компилируем изходен код и типов набор (в TeX) за кръстосано свързана документация, използвайки оригиналния файл. Езикът, използван за разработване на тези усъвършенствани версии на TeX, се нарича WEB, смес от програми DEC PDP-10 Pascal, за да се гарантира преносимост.

Ревизирана нова версия на TeX, публикувана през 1982 г. и се нарича TeX82. Основната промяна е замяната на оригиналния алгоритъм за сричкопренасяне с новонаписания алгоритъм от Frank Liang. За да осигури преносимост между различни платформи, вместо да използва плаваща запетая, TeX82 използва аритметика с фиксирана запетая заедно с реален, пълен с Тюринг език за програмиране. През 1989 г. бяха пуснати нови версии на TeX и Metafont. Така версия 3.0 на TeX улеснява 8-битови входове, позволявайки 256 различни знака в текста. След версия 3 актуализациите се обозначават чрез добавяне на допълнителна цифра в края на десетичната запетая, например текущата версия на TeX се обозначава като 3.14159265. Тази версия е последно актуализирана на 12-1-2014.

## TeX вход ##

Входен файл към TEX може да бъде подготвен с текстов редактор, като се използва обикновен текст. За разлика от типичния Word процесор, този входен файл не позволява никакви невидими контролни знаци. Един файл може да бъде вграден в друг файл, съдържащ дефиниции на макроси и спомагателни дефиниции, които подобряват възможностите на TeX. Ако инсталацията на TeX идва с някакви макро файлове, локалната информация за TeX демонстрира използването на макро файлове. Стандартната форма на TeX интегрира комбинация от макроси и други дефиниции, известни като обикновен TEX.

Въз основа на точното познаване на размерите на всички знаци и символи, той изчислява оптималната организация на буквите на ред и редовете на страницата. По време на обработката на документа се създава .dvi файл, където „dvi“ означава „независим от устройство“. Програмите за драйвери на устройството са необходими за отпечатване или предварителен преглед на документа с dvi разширение. В наши дни генерирането на dvi се заобикаля от често използван pdf-TeX. В рамките на инсталацията на TeX няма налични предварителни познания за шрифтове, така че външни файлове с шрифтове, които са част от локалната TeX среда, се използват за получаване на информация за документа.

## Наборна система ##

Около 300 примитиви (команди) могат да бъдат разбрани от базовата TeX система. Примитивите са команди от ниско ниво, поради което обикновеният потребител рядко ги използва директно и повечето функции се изпълняват от форматирани файлове. Тези форматирани файлове са предварително заредени изображения на паметта на TeX, които са последвани от зареждането на големи колекции от макроси. Оригиналният формат по подразбиране на езика, т.е. обикновен TeX, добавя около 600 команди.

Обратна наклонена черта, групирана с къдрави скоби, обозначава началото на TeX команди. Тъй като TeX е език, базиран на макроси и токени, почти всички синтактични характеристики на TeX могат да се променят по време на изпълнение, включително дефинирани от потребителя, с изключение на неразширяеми токени, които след това се изпълняват. Самото разширяване е практически безпроблемно. Някои команди трябва да идват след аргументи, които помагат да се обясни функцията на дадена команда. Например, командата \vskip насочва TEX да пропусне страницата надолу/нагоре, последвано от аргумент, определящ колко място да пропусне.

## Версии ##

LaTeX е най-често използваният формат, който първоначално е разработен от Лесли Лампорт. LaTeX интегрира различни стилове на документи за файлове, писма, книги и слайдове и предлага препращане и автоматично номериране за различни секции и математически изрази. AMS-TeX е друг популярен формат, разработен от Американското математическо общество.

AMS-TeX предлага много по-удобни за потребителя команди, които могат да бъдат предефинирани от списания, за да паснат на техния местен стил. LaTeX може да се възползва от предимствата на AMS-TeX, като използва AMS "пакетите", които след това се наричат като AMS-LaTeX. ConTeXt е друг формат, написан от Hans Hagen, използван главно за настолни публикации.

Софтуерът TeX предлага няколко функции, които са били недостъпни или с по-ниско качество в други системи за набор по време на създаването му. Някои от иновативните функции на този език се основават на интересни алгоритми, извлечени от тезите на учениците на Кнут. Докато други програми за набор вече включват полезни функции на TeX в своите програми.

## Препратки ##

* [Система за набор на TeX](https://en.wikipedia.org/wiki/TeX)
