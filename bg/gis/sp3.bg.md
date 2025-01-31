{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - NGS SP3 файл",
  "description":"Научете за SP3 файловия формат и API, които могат да създават и отварят SP3 файлове.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Какво е SP3 файл?

Файл с разширение .sp3 е орбитален формат на National Geodetic Survey (NGS) за съхраняване на орбитална информация. Това е разширение на форматите SP1 и SP2 на NGS и включва информация за корекция на сателитния часовник, която се изчислява едновременно с орбитите. Основно се основава на позиция и часовник и не включва скорости. Форматът е предложен в Remondi, 1989 г. и е приет през 1991 г. В допълнение към информацията за корекция на сателитния часовник, той включва информация като показатели за точност на орбитата, редове за коментари, GPS седмица и секунди от седмицата, свързани с първата епоха. SP3 файловете могат да се отварят с Wolfram Research Mathematica.

## SP3 файлов формат - повече информация

SP3 файловете се записват на диск във файлов формат ASCII и съдържанието му може да се отвори във всеки текстов редактор за преглед. Структурата на SP3 файл може да се види от следното изображение.

{{< figure src="../sp3-file-format.png" title="" >}}

## Препратки

* [Разширен стандартен продукт 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,%20по-гъвкава%20заглавна%20структура)
* [Разширяване на стандартните GPS орбитални формати на Националното геодезическо проучване](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

